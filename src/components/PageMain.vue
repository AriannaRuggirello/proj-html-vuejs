<script >
import MainSpecialEvents from '../components/MainSpecialEvents.vue'


export default {
    name: 'PageMain',
    components: {
        MainSpecialEvents,
    },
    data() {
        return {
            specialEvents: [
                {
                    img: '../../public/images/avada-nightclub-events-6-400x225.jpg',
                    text: 'DJ Fusion',
                    date: 'August 19,2022 @ 8.00 am',
                },

                {
                    img: '../../public/images/avada-nightclub-events-5-400x225.jpg',
                    text: 'House Nation',
                    date: 'August 19,2022 @ 8.00 am',
                },

                {
                    img: '../../public/images/avada-nightclub-events-4-400x225.jpg',
                    text: 'Jazz Night',
                    date: 'August 19,2022 @ 8.00 am',
                },

                {
                    img: '../../public/images/avada-nightclub-events-3-400x225.jpg',
                    text: 'VIP Taster Session',
                    date: 'August 19,2022 @ 8.00 am',
                },

                {
                    img: '../../public/images/avada-nightclub-events-2-400x225.jpg',
                    text: 'Funky House Rave',
                    date: 'August 19,2022 @ 8.00 am',
                },

                {
                    img: '../../public/images/avada-nightclub-events-1-400x225.jpg',
                    text: 'Urban Vibes',
                    date: 'August 19,2022 @ 8.00 am',
                },

            ]
        }
    }
}
</script>

<template>
    <main>
        <!-- club section -->
        <section class="theClub">

            <div class="container">
                <!-- testo -->
                <div class="row text-center justify-content-center">
                    <div class="col-lg-7">
                        <h4 class="blu-txt">WELCOME TO AVADA</h4>
                        <h2>have the night of your life</h2>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus, dolores cumque! Officia vero
                            quae explicabo fugiat earum, expedita quidem optio quasi voluptate veniam cupiditate nulla
                            beatae
                            dolor porro inventore eos.</p>
                    </div>

                </div>
                <!-- immagini -->
                <div class="row text-center ">
                    <!-- 4img cards -->
                    <div class="col text-end info">
                        <img src="../../public/images/avada-nightclub-dancelounge-small.jpg" alt="">
                        <div class="info-img">
                            <span>dance lounge</span>
                            <hr>
                        </div>
                    </div>

                    <div class="col text-start info">

                        <img src="../../public/images/avada-nightclub-rooftoplounge-small.jpg" alt="">
                        <div class="info-img">
                            <span>rooftop bar</span>
                            <hr class="red">
                        </div>

                    </div>

                    <div class="col text-end info ">

                        <img src="../../public/images/avada-nightclub-viplounge-small.jpg" alt="">
                        <div class="info-img">
                            <span>vip lounge</span>
                            <hr class="gold">
                        </div>

                    </div>

                    <div class="col text-start info">

                        <img src="../../public/images/avada-nightclub-events-5-600x338.jpg" alt="">
                        <div class="info-img">
                            <span>resident dj</span>
                            <hr class="red">
                        </div>

                    </div>
                </div>
            </div>

        </section>

        <!-- dj set section -->
        <section class="dj-set">

            <div class="row">
                <div class="col-lg-6 info">
                    <!-- img -->
                    <img src="../../public/images/avada-nightclub-resident-profile.jpg" alt="">
                    <!-- scritta sopra img -->
                    <div class="info-button">
                        <h4 class="red-txt">RESIDENT DJ</h4>
                        <h2>Dj Avada</h2>
                        <button class="blue">view profile</button>
                    </div>
                </div>
                <div class="col-lg-6 info">
                    <!-- img -->
                    <img src="../../public/images/avada-nightclub-lisahouse-inset-new.jpg" alt="">
                    <!-- scritta sopra img -->
                    <div class="info-button">
                        <h4 class="blu-txt">SPECIAL GUEST DJ </h4>
                        <h2>Dj Blondie</h2>
                        <button class="red">view profile</button>
                    </div>
                </div>
            </div>


        </section>

        <!-- special events section -->
        <section class="special-events">

            <div class="overlay">
                <div class="row text-center row-cols-1">
                    <!-- scritte centrali -->
                    <div class="col">
                        <h4 class="red-txt">SPECIAL EVENTS</h4>
                        <h2>for your diary</h2>
                    </div>
                    <!--6 img e info -->
                    <div class="col">
                        <div class="container">
                            <div class="row">
                                <MainSpecialEvents v-for="specialEvent in specialEvents" :details="specialEvent" />
                            </div>
                            <!-- button -->
                            <div class="col">
                                <button class="red">rsvp now</button>
                            </div>
                        </div>

                    </div>
                </div>
            </div>
        </section>

        <!-- vip section -->
        <section class="vip">

            <div class="row justify-content-center align-items-center">
                <div class="col-lg-5">
                    <!-- info sx -->
                    <h4 class="blu-txt">SPECIAL GUEST DJ </h4>
                    <h2>esclusive vip lounge</h2>
                </div>
                <div class="col-lg-2">
                    <!-- button dx -->
                    <button class="red">
                        join the club
                    </button>
                </div>
            </div>

        </section>


    </main>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;
@use '../style/general.scss' as *;



.theClub {
    background-image: url(../../public/images/avada-nightclub-cloud-background.jpg);
    background-size: cover;
    padding: 100px 0;
    color: gray;

    .row>* {
        padding-right: calc(var(--bs-gutter-x) * 0);
        padding-left: calc(var(--bs-gutter-x) * 0);
    }
}

.info {
    position: relative;
    color: white;

    img {
        width: 600px;
        height: 338px;
    }

    .info-img {
        display: flex;
        align-items: center;
        position: absolute;
        right: 0;
        bottom: 10%;

        span {
            font-size: x-large;
            padding-right: 5px;

        }

        hr {
            width: 400px;
            opacity: inherit;
            color: $primary-color;

        }

        .red {
            color: $secondary-color;
        }

        .gold {
            color: gold;
        }
    }


}

.dj-set {
    .row>* {
        padding-right: calc(var(--bs-gutter-x) * 0);
        padding-left: calc(var(--bs-gutter-x) * 0);
    }

    img {
        width: 100%;
        height: 500px;
        object-fit: cover;
        position: relative;
    }

    .info-button {
        position: absolute;
        top: 10%;
        left: 10%;
    }

    .blue:hover {}

}

.special-events {
    padding: 150px 0;
    background-image: url(../../public/images/avada-nightclub-homepage-events-background-new.jpg);
    background-size: cover;
    color: white;
    position: relative;


}

.vip {
    background-image: url(../../public/images/avada-nightclub-vip-hero-new.jpg);
    background-size: cover;
    padding: 100px 0;
}
</style>
