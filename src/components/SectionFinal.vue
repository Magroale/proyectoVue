<template>
    <footer>
        <div class="container text-center rounded container-subscribe p-5 mb-5">
            <h2 class="text-white subtitle-subscribe my-5 mx-auto w-75">Subscribe and get exclusive deals & offer</h2>
            <div class="input-group align-items-center w-50 my-5 mx-auto">
                <input type="text" class="form-control rounded px-5 py-3" placeholder="Enter your mail"
                    aria-label="Recipient's username" aria-describedby="basic-addon2">
                <img class="position-absolute mx-3" src="../assets/icons/mail-ico.png" alt="" width="">
                <div class="input-group-append mx-2">
                    <button class="btn btn-outline-light py-3" type="button">Subscribe</button>
                </div>
            </div>
        </div>
        <div class="container pt-5">
            <div class="row">
                <div class="col-5">
                    <h3 class="title-trabook d-flex align-items-center">Trabook <img class="mx-2" src="../assets/icons/favicon.png"
                            alt="">
                    </h3>
                    <p class="light-text">Book your trip in minute, get full Control for much longer.</p>
                    <ul class="list-unstyled d-flex social-list">
                        <li><a href=""><img src="../assets/icons/facebook.png" alt=""></a></li>
                        <li class="mx-4"><a href=""><img src="../assets/icons/instagram.png" alt=""></a></li>
                        <li><a href=""><img src="../assets/icons/twitter.png" alt=""></a></li>
                    </ul>
                </div>
                <div class="col">
                    <h3>Company</h3>
                    <ul class="list-unstyled light-text">
                        <li>About</li>
                        <li>Careers</li>
                        <li>Logistic</li>
                        <li>Privacy & Policy</li>
                    </ul>
                </div>
                <div class="col">
                    <h3>Contact</h3>
                    <ul class="list-unstyled light-text">
                        <li>Help/FAQ</li>
                        <li>Press</li>
                        <li>Affilates</li>
                    </ul>
                </div>
                <div class="col">
                    <h3>More</h3>
                    <ul class="list-unstyled light-text">
                        <li>Press Centre</li>
                        <li>Our Blog</li>
                        <li>Low fare tips</li>
                    </ul>
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between container-copyright">
                <p>Copyright, Trabook 2022. All rights reserved | Developed by</p>
                <p>Terms & Conditions</p>
            </div>
        </div>

    </footer>
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
footer {
    background-color: #F7F8FC;
}

.container-subscribe {
    background-image: url("../assets/back-subscribe.svg");
    background-color: #FA7436;
    background-position: center;
    background-size: cover;
}

.title-trabook {
    font-family: 'Volkhov', serif;
}

.social-list li {
    display: flex;
    background-color: #ffffff;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    justify-content: center;
    align-items: center;
    box-shadow: 1px 1px 10px #a8a8a8;
}

.social-list li:nth-child(2) {
    background-color: #FA7436;
    width: 48px;
    height: 48px;
}
</style>