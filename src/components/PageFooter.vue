<script >

import FooterEvents from '../components/FooterEvents.vue'
import FooterLinks from '../components/FooterLinks.vue'


export default {
    name: 'PageFooter',
    components: {
        FooterEvents,
        FooterLinks,
    },
    data() {
        return {
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
            ],
            footerLink: [
                {
                    text: 'Avada Night Club',
                    state: false,
                    url: '#',
                },
                {
                    text: '100 Night Club Blvd',
                    state: false,
                    url: '#',
                },
                {
                    text: 'Beverly Hills',
                    state: false,
                    url: '#',
                }, {
                    text: 'hi@your-demain.com',
                    state: true,
                    url: '#',
                }, {
                    text: '+1 (500) 000 000',
                    state: false,
                    url: '#',
                },
            ]
        }
    }

}
</script>

<template>
    <footer>
        <div class="container">
            <!-- tre colonne -->
            <div class="row text-center justify-content-between">
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
                            <!-- logo -->
                            <img src="../../public/images/avada-nightclub-logo-2x-200x66.png" alt="">
                        </div>

                        <div class="col">
                            <ul>
                                <FooterLinks v-for="link in footerLink" :details="link"
                                    :class="link.state ? 'active' : ''" />
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
                    <img class="space" src="../../public/images/avada-nightclub-footer-rooftop-400x171.jpg" alt="">

                    <img src="../../public/images/avada-nightclub-footer-dancelounge-400x171.jpg" alt="">
                </div>
                <!-- copyright -->
                <div class="row">
                    <div class="col copy">
                        <p>
                            Avada Theme by <a href="#">ThemeFusion</a> | All Right Reserved | Powered by
                            <a href="#">Wordpress</a> Wordpress
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;
@use '../style/general.scss' as *;

footer {
    background-image: url(../../public/images/avada-nightclub-footer-background-final-2.jpg);
    background-position: bottom;
    background-size: cover;
    background-repeat: no-repeat;
    padding: 80px 0;

    li {

        &.active,
        &:hover {

            color: $primary-color;

        }
    }



    .copy {
        padding-top: 150px;

    }

    h4,
    p {
        color: white;
    }

    a {
        color: $primary-color;
    }

}
</style>
