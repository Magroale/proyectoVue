<template>
    <div class="d-flex flex-column justify-content-center" style="background-color: #f7f8fc; padding-top: 8rem;">
        <div class="d-flex flex-column container container-mid mt-1 align-items-center justify-content-center" style=" border: 10px; max-width: 80vw;">
            <div class="bloque">
                <h1 style="font-size: 50px;"><span style="color: black;">Things you need</span> <span
                        style="color: #fa7436;">to do</span></h1>
                <p class="Parrafo">we ensure that you'll embark on a perfectly planned, safe vacation at a price you can
                    afford.</p>
            </div>
        </div>

        <div class="d-flex container container-mid mt-1 justify-content-evenly" style="padding-top: 2rem; padding-bottom: 2rem; border: 10px; max-width: 80vw;">
            <div class="card border border-warning shadow-0 mb-3" style="max-width: 18rem; max-height: 18rem;" 
            v-for="(carta, index) in infoCartas" :key="index">
                <div class="card-header"><i :class="carta.icono" :style="carta.estilo"></i></div>
                <div class="card-body">
                    <h5 class="card-title">{{ carta.titulo }}</h5>
                    <p class="card-text">{{ carta.texto }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    },
    data() {
        return {
            infoCartas: [
                {
                    icono: "fas fa-rectangle-list fa-3x",
                    estilo: "color:#fa7436;",
                    titulo: "Sign up",
                    texto: "Some quick example text to build on the card title and make up the bulk of the card's content."
                },
                {
                    icono: "fas fa-wallet fa-3x",
                    estilo: "color:#4086f4;",
                    titulo: "Worth of Money",
                    texto: "After successful acces then book from exclusive deals & pricing."
                },
                {
                    icono: "fas fa-location-dot fa-3x",
                    estilo: "color: #ffb60a;",
                    titulo: "Exciting Travel",
                    texto: "Start and a explore a wide of exciting travel experience."
                },
            ],
        }
    },
    methods: {
    },
}
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Centrado {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0px;
    vertical-align: middle;
}

.bloque {
    display: block;
    justify-content: space-between;
    align-items: center;
    margin-left: 50px;
    margin-right: 50px;
    max-width: 40em;
    text-align: center;
}

.Parrafo {
    font-size: 18px;
    color: 666666;
}

.Izquierda,
.Derecha {
    flex: 1;
    text-align: center;
    padding-left: 10px;
}

.Izquierda {
    display: flex;
    margin-right: 20px;
}

.Derecha {
    display: flex;
    margin-left: 40px;
}

.ParrafoPrecio,
.ParrafoPrecioRayado {
    font-weight: bold;
}

.ParrafoPrecio {
    color: #fa7436;
    background-color: #ffe7db;
    border-radius: 10px;
}

.ParrafoPrecioRayado {
    text-decoration: line-through;
    margin-right: 10px;
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

h1 {
    color: black;
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

body {
    width: 1170px;
    margin: 0 auto;
    padding: 20px;
    font-family: 'Times New Roman', Times, serif;
}
</style>