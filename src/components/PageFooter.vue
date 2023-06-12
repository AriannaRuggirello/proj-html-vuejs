<script >

import FooterEvents from '../components/FooterEvents.vue'

export default {
    name: 'PageFooter',
    components: {
        FooterEvents,
    },
    events: [
        {
            img: '../../public/images/avada-nightclub-events-6-66x66.jpg',
            text: 'DJ Fusion',
            date: 'August 19,2022 @ 8.00 am',


        },
        {
            img: '../../public/images/avada-nightclub-events-5-66x66.jpg',
            text: 'House Nation',
            date: 'August 19,2022 @ 8.00 am',


        }, {
            img: '../../public/images/avada-nightclub-events-4-66x66.jpg',
            text: 'Jazz Night',
            date: 'August 19,2022 @ 8.00 am',


        },
    ]
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

                    <FooterEvents v-for="event in events" :details="event" />

                    <a href=" #">View All Events</a>
                </div>

                <!-- colonna link -->
                <div class="col">
                    <div class="row row-cols-1">
                        <div class="col space">
                            <img src="../../public/images/avada-nightclub-logo-2x-200x66.png" alt="">

                        </div>

                        <div class="col space">
                            <ul>
                                <li>link</li>
                                <li>link</li>
                                <li>link</li>
                                <li>link</li>
                                <li>link</li>

                            </ul>
                        </div>

                        <div class="col space align-self-center">
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
                    <img class="space" src="../../public/images/avada-nightclub-footer-rooftop-400x171.jpg" alt="">

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


    .space {
        padding-bottom: 40px;
    }

    h3 {
        color: $primary-color;
    }

    span {
        color: #68665a;
    }

    li {
        list-style: none;
    }

    i {

        padding-right: 30px;
    }
}
</style>
