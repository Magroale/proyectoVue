<template>
    <div class="d-flex mx-auto align-items-center justify-content-center py-5"
        style="border: 10px; max-width: 80vw; background-color: #ffffff;">

        <div class="d-flex flex-column px-5 w-50 p-3 container container-mid mt-1 align-self-start">
            <h1 class="titulo"> What people say <span style="color:orange;">about us.</span></h1>
            <p class="w-75 p-3">Our clients send bunch of smilies with our services and we love them</p>
            <div class="d-flex flex-row justify-content-start mb-3"
                style="padding-bottom: 2rem;">
                <button class="EstiloBotones" style="margin-right: 20px;" :disabled="currentPage === 0" @click="prevPage"><i
                        class="fas fa-arrow-left-long"></i></button>
                <button class="EstiloBotones"><i class="fas fa-arrow-right-long" :disabled="currentPage === totalPages - 1"
                        @click="nextPage"></i></button>
            </div>
        </div>

        <div class="d-flex mx-auto justify-content-center pt-5" style="width:450px; background-color: #ffffff; ">
            <div class="card w-100" style="max-height: 310px;" v-for="(carta, index) in displayedCards" :key="index">
                <div class="card-body">
                    <img src="https://img.freepik.com/free-photo/young-bearded-man-with-striped-shirt_273609-5677.jpg?size=626&ext=jpg&ga=GA1.1.1448711260.1696291200&semt=ais"
                        class="profile-image" alt="Sunset Over the Sea" />
                    <p class="card-text align-self-start">{{carta.text_Comments}}</p>
                    <h4>{{ carta.personName }}</h4>
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
            infoComentarios: [],
            cardsPerPage: 1,
            currentPage: 0,
        }
    },
    computed: {
        displayedCards() {
            const start = this.currentPage * this.cardsPerPage;
            const end = start + this.cardsPerPage;
            return this.infoComentarios.slice(start, end);
        },
    },

    methods: {
        prevPage() {
            if (this.currentPage > 0) {
                this.currentPage--;
            }
        },
        nextPage() {
            const totalPages = Math.ceil(this.infoComentarios.length / this.cardsPerPage);
            if (this.currentPage < totalPages - 1) {
                this.currentPage++;
            }
        },
    },


    mounted() {
        axios.get('https://backend-para-proyecto-parznk944.vercel.app/vista_comentario')
            .then(response => {
                this.infoComentarios = response.data;
                console.log(response.data)
            })
            .catch(error => {
                console.error('Error fetching data:', error);
            });
    },
}
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.titulo {
    font-size: 60px;
}

.cartas {
    font-size: 14px;
}

.profile-image {
    position: absolute;
    top: 0;
    left: 0;
    width: 70px;
    height: 70px;
    background-size: cover;
    border-radius: 50%;
    transform: translate(-50%, -50%);
}

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