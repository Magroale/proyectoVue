<template>
    <div class="d-flex flex-column pb-5 mb-5 justify-content-center align-items-center" style="background-color: #f7f8fc; padding-top: 8rem;">
        <div class="d-flex flex-column container container-mid mt-1 align-items-center justify-content-center"
            style=" border: 10px; max-width: 80vw;">
            <h1 style="font-size: 50px;"><span style="color: black;">Get update with</span> <span
                    style="color: #fa7436;">latest blog</span></h1>
        </div>

        <div class="d-flex justify-content-sm-evenly" style="border: 10px; max-width: 80vw;">
            <div class="card" style="width: 25rem; margin: 1em;" v-for="(carta, index) in displayedCards" :key="index">
                <img src="https://www.bestosakahotels.com/data/Photos/940x450/4079/407901/407901420/osaka-basket-apartment-photo-2.JPEG" class="card-img-top" alt="Sunset Over the Sea" />
                <div class="card-body d-flex flex-column">
                    <div class="d-flex justify-content-between">
                        <h5 class="card-title">{{ carta.news }}</h5>
                    </div>

                    <div class="d-flex justify-content-between">
                        <p class="card-title">July 27, 2021</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="d-flex flex-row container container-mid align-items-center justify-content-center"
            style=" border: 10px; max-width: 80vw;">
            <button class="EstiloBotones" style="margin-right: 20px;" :disabled="currentPage === 0" @click="prevPage"><i class="fas fa-arrow-left-long"></i></button>
            <button class="EstiloBotones"><i class="fas fa-arrow-right-long" :disabled="currentPage === totalPages - 1" @click="nextPage"></i></button>
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
        axios.get('http://127.0.0.1:8000/home_page')
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