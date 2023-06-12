<script >


export default {
    name: 'PageFooter',

}





</script>

<template>
    <footer>
        <div class="container">
            <!-- tre colonne -->
            <div class="row text-center">
                <!-- colonna eventi -->
                <div class="col">
                    <h4>EVENTS</h4>
                    <!-- foto e paragrafo -->
                    <div class="row">
                        <div class="col text-end">
                            <!-- immagine -->
                            <img src="../../public/images/avada-nightclub-events-6-66x66.jpg" alt="">
                        </div>
                        <div class="col text-start">
                            <!-- titolo piu span -->
                            <h3>TITOLO</h3>
                            <span>piccolo paragrafo</span>
                        </div>
                    </div>

                    <!-- foto e paragrafo -->
                    <div class="row">
                        <div class="col text-end">
                            <!-- immagine -->
                            <img src="../../public/images/avada-nightclub-events-6-66x66.jpg" alt="">
                        </div>
                        <div class="col text-start">
                            <!-- titolo piu span -->
                            <h3>TITOLO</h3>
                            <span>piccolo paragrafo</span>
                        </div>
                    </div>

                    <!-- foto e paragrafo -->
                    <div class="row">
                        <div class="col text-end">
                            <!-- immagine -->
                            <img src="../../public/images/avada-nightclub-events-6-66x66.jpg" alt="">
                        </div>
                        <div class="col text-start">
                            <!-- titolo piu span -->
                            <h3>TITOLO</h3>
                            <span>piccolo paragrafo</span>
                        </div>
                    </div>

                    <a href="#">View All Events</a>
                </div>

                <!-- colonna link -->
                <div class="col">
                    <div class="row row-cols-1">
                        <div class="col">
                            <img src="../../public/images/avada-nightclub-logo-2x-200x66.png" alt="">

                        </div>

                        <div class="col">
                            <ul>
                                <li>link</li>
                                <li>link</li>
                                <li>link</li>
                                <li>link</li>
                                <li>link</li>

                            </ul>
                        </div>

                        <div class="col">
                            <i class="fa-brands fa-facebook-f"></i>
                            <i class="fa-brands fa-twitter"></i>
                            <i class="fa-brands fa-instagram"></i>
                            <i class="fa-brands fa-youtube"></i>
                        </div>

                    </div>

                </div>

                <!-- colonna venues -->
                <div class="col">
                    <h4>VENUES</h4>
                    <img src="../../public/images/avada-nightclub-footer-rooftop-400x171.jpg" alt="">

                    <img src="../../public/images/avada-nightclub-footer-dancelounge-400x171.jpg" alt="">
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;

footer {
    background-image: url(../../public/images/avada-nightclub-footer-background-final-2.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    height: 500px;
    color: white;
    padding: 80px 0;




    h3 {
        color: $primary-color;
    }

    span {
        color: #68665a;
    }

    li {
        list-style: none;
    }
}
</style>
