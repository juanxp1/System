<template>
    <div>
        <div class="container d-flex flex-wrap justify-content-between mt-5">
            <div class="card bg-dark text-white mb-3" style="width: 18rem;">
                <img class="card-img-top" :src="camara" alt="Card image cap">
                <div class="card-body">
                    <h5 class="card-title">Sistemas de seguridad especiales</h5>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the
                        card's
                        content.</p>
                    <a href="#" class="btn btn-primary">Read More</a>
                </div>
            </div>
            <div class="card bg-dark text-white mb-3" style="width: 18rem;">
                <img class="card-img-top" :src="candado" alt="Card image cap">
                <div class="card-body">
                    <h5 class="card-title">Sistemas de Seguridad para hogares</h5>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the
                        card's
                        content.</p>
                    <a href="#" class="btn btn-primary">Read More</a>
                </div>
            </div>
            <div class="card bg-dark text-white mb-3" style="width: 18rem;">
                <img class="card-img-top" :src="seguridad" alt="Card image cap">
                <div class="card-body">
                    <h5 class="card-title">Sistemas de seguridad para la Oficina</h5>
                    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the
                        card's
                        content.</p>
                    <a href="#" class="btn btn-primary">Read More</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import camara from '../assets/page1-img1.jpg'
import candado from '../assets/page1-img2.jpg'
import seguridad from '../assets/page1-img3.jpg'

</script>

<style  scoped>
.container {
    width: 75%;
}

.btn{
    background-color: #343a40;
}

@media (max-width: 767px) {
    .container {
        width: 75%;
    }

    .card {
        width: 100%;
    }
}
</style>