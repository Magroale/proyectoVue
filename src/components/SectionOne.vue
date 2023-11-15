<template>
    <div class="d-flex-column justify-content-center">
        <div class="d-flex mx-auto justify-content-center py-5"
            style="border: 10px; background-color: #ffffff; max-width: 80vw;">
            <div class="d-flex flex-column px-5 container container-mid mt-1 align-items-center justify-content-center"
                style="max-width: 600px;">

                <h1 class="titulo"> Get started your exciting <span style="color:orange;">journey</span> with us.</h1>
                <p>A Team of experience tourism professionals will provide you ith the best advice and tips for your
                    desire
                    place</p>

                <button type="button" class="btn btn-outline-warning" data-mdb-ripple-color="dark"><span>Discover
                        Now</span></button>

            </div>

            <div class="d-flex flex-column overflow-visible flex-shrink-0 bg-image text-center shadow-1-strong rounded text-white rounded-circle"
                style="background-image: url('https://mdbcdn.b-cdn.net/img/new/slides/003.webp'); width:450px; height:450px;">

                <div class="col align-self-start card mt-5 bg-white">
                    <div class="row g-0">
                        <div class="col-md-4 d-flex align-items-center">
                            <i class="fas fa-trophy fa-2x" style="color: orange;"></i>
                        </div>
                        <div class="col-md-8 d-flex align-items-center">
                            <div class="card-body">
                                <h5 class="card-title text-black cartas">Best Tour Awards</h5>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col align-self-end card mb-5 mt-5 bg-white">
                    <div class="row g-0">
                        <div class="col-md-4 d-flex align-items-center justify-content-center">
                            <i class="fas fa-location-dot fa-2x" style="color: orange;"></i>
                        </div>
                        <div class="col-md-8 d-flex align-items-center">
                            <div class="card-body">
                                <h5 class="card-title text-black cartas">Explore</h5>
                                <p class="card-text text-black cartas">
                                    Every cornar of the world with us.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col align-self-start card mb-5 bg-white">
                    <div class="row g-0">
                        <div class="col-md-4 d-flex align-items-center justify-content-center">
                            <i class="fas fa-star fa-2x" style="color: orange; line-height: 1;"></i>
                        </div>
                        <div class="col-md-8 d-flex align-items-center">
                            <div class="card-body">
                                <h5 class="card-title text-black cartas">27K</h5>
                                <p class="card-text text-black cartas">
                                    Customer Reviwd.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="d-flex container mx-auto row align-items-center justify-content-center p-3 bg-white shadow-lg mb-5">
            <div class="container row" style="border: 10px; background-color: #fefcfb; max-width: 60vw;">
                <div class="col d-flex flex-column">
                    <span class="dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button"
                            data-mdb-toggle="dropdown" aria-expanded="false">
                            Dropdown link
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                            <li>
                                <a class="dropdown-item" href="#">Action</a>
                            </li>
                            <li>
                                <a class="dropdown-item" href="#">Another action</a>
                            </li>
                            <li>
                                <a class="dropdown-item" href="#">Something else here</a>
                            </li>
                        </ul>
                    </span>
                    <p> Something else here</p>
                </div>
                <div class="col d-flex flex-column">
                    <span class="dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button"
                            data-mdb-toggle="dropdown" aria-expanded="false">
                            Dropdown link
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                            <li>
                                <a class="dropdown-item" href="#">Action</a>
                            </li>
                            <li>
                                <a class="dropdown-item" href="#">Another action</a>
                            </li>
                            <li>
                                <a class="dropdown-item" href="#">Something else here</a>
                            </li>
                        </ul>
                    </span>
                    <p> Something else here</p>
                </div>
                <div class="col d-flex flex-column">
                    <span class="dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button"
                            data-mdb-toggle="dropdown" aria-expanded="false">
                            Dropdown link
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                            <li>
                                <a class="dropdown-item" href="#">Action</a>
                            </li>
                            <li>
                                <a class="dropdown-item" href="#">Another action</a>
                            </li>
                            <li>
                                <a class="dropdown-item" href="#">Something else here</a>
                            </li>
                        </ul>
                    </span>
                    <p> Something else here</p>
                </div>
                <div class="col row">
                    <button type="button" class="btn btn-warning">Explore now</button>
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

        }
    },
    methods: {
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
</style>