<template>
    <div class="d-flex flex-column justify-content-center align-items-center"
        style="background-color: #f7f8fc; padding-top: 2rem; padding-bottom: 8rem;">
        <div class="d-flex flex-column container container-mid mt-1 align-items-center justify-content-center"
            style=" border: 10px; max-width: 80vw;">
            <h1 style="font-size: 50px;"><span style="color: black;">Best</span> <span style="color: #fa7436;">vacation
                    plan</span></h1>
            <p class="Parrafo">Plan your perfect vacation with our travel agency. Choose among hundreds of all-inclsuive
                offers!</p>
        </div>

        <div class="d-flex flex-row container container-mid align-items-center justify-content-end mb-3"
            style=" border: 10px; max-width: 80vw; padding-bottom: 2rem;">
            <button class="EstiloBotones" style="margin-right: 20px;" :disabled="currentPage === 0" @click="prevPage"><i class="fas fa-arrow-left-long"></i></button>
            <button class="EstiloBotones"><i class="fas fa-arrow-right-long" :disabled="currentPage === totalPages - 1" @click="nextPage"></i></button>
        </div>

        <div class="d-flex justify-content-evenly align-items-center" style="border: 10px; max-width: 80vw;">
            <div class="card d-flex justify-content-center" style="width: 25rem; margin: 1em;"
                v-for="(carta, index) in displayedCards" :key="index">
                <!-- <img :src="carta.url" class="card-img-top"
                    alt="Sunset Over the Sea" /> -->
                <img src="https://wydjourneys.com/wp-content/uploads/2022/03/Vatican3-700x500.jpg" class="card-img-top" alt="Sunset Over the Sea" />
                <div class="card-body d-flex flex-column">
                    <div class="d-flex justify-content-between">
                        <h5 class="card-title">{{ carta.country }}, {{ carta.location }}</h5>
                        <div class="d-flex flex-row mb-3">
                            <h5 class="card-title">${{carta.price-(carta.discountPercentage*carta.price)}}</h5>
                        </div>
                    </div>

                    <div class="d-flex justify-content-between">
                        <div class="d-flex flex-row">
                            <i class="fas fa-location-dot fa-1x pt-1"></i>
                            <h5 class="card-title">{{ carta.numberDays }} Days Trip</h5>
                        </div>
                        <div class="d-flex justify-content-evenly">
                            <i class="fas fa-star fa-1x pt-1"></i>
                            <p>{{ carta.score }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import axios from 'axios'
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    },
    data() {
        return {
            infoCartas: [],
            cardsPerPage: 4,
            currentPage: 0,
        }
    },

    computed: {
        displayedCards() {
            const start = this.currentPage * this.cardsPerPage;
            const end = start + this.cardsPerPage;
            return this.infoCartas.slice(start, end);
        },
    },

    methods: {
        prevPage() {
            if (this.currentPage > 0) {
                this.currentPage--;
            }
        },
        nextPage() {
            const totalPages = Math.ceil(this.infoCartas.length / this.cardsPerPage);
            if (this.currentPage < totalPages - 1) {
                this.currentPage++;
            }
        },
    },

    mounted() {
        axios.get('https://backend-para-proyecto-parznk944.vercel.app/home_page')
            .then(response => {
                this.infoCartas = response.data;
                console.log(this.infoCartas)
            })
            .catch(error => {
                console.error('Error fetching data:', error);
            });
    },
}
</script>
  
<style scoped>
.EstiloBotones {
    border-radius: 20px;
    background-color: white;
    color: grey;
    border: 2px solid gray;
}

.EstiloBotones:hover {
    background-color: #fa7436;
}
</style>