<script >


export default {
    name: 'PageMain',

}
</script>

<template>
    <main>
        <section class="theClub">
            <div class="container">
                <!-- testo -->
                <div class="row text-center justify-content-center">
                    <div class="col-lg-7">
                        <h4>WELCOME TO AVADA</h4>
                        <h2>have the night of your life</h2>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus, dolores cumque! Officia vero
                            quae explicabo fugiat earum, expedita quidem optio quasi voluptate veniam cupiditate nulla
                            beatae
                            dolor porro inventore eos.</p>
                    </div>

                </div>
                <!-- immagini -->
                <div class="row text-center ">

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

        <section class="dj-set">

            <div class="row">
                <div class="col-lg-6 info">
                    <img src="../../public/images/avada-nightclub-resident-profile.jpg" alt="">
                    <div class="info-button">
                        <h4 class="blu-txt">RESIDENT DJ</h4>
                        <h2>Dj Avada</h2>
                        <button class="blu-button">view profile</button>
                    </div>
                </div>
                <div class="col-lg-6 info">
                    <img src="../../public/images/avada-nightclub-lisahouse-inset-new.jpg" alt="">
                    <div class="info-button">
                        <h4 class="red-txt">SPECIAL GUEST DJ </h4>
                        <h2>Dj Blondie</h2>
                        <button class="red-button">view profile</button>
                    </div>
                </div>
            </div>


        </section>

        <section class="special-events">
            <div class="row text-center row-cols-1">
                <div class="col">
                    <h4 class="red-txt">SPECIAL EVENTS</h4>
                    <h2>for your diary</h2>
                </div>

                <div class="col">
                    <div class="container">
                        <div class="row">
                            <div class="col">
                                <img src="../../public/images/avada-nightclub-events-6-400x225.jpg" alt="">
                                <h3 class="red-txt">titolo</h3>
                                <span>data</span>
                            </div>

                            <div class="col">
                                <img src="../../public/images/avada-nightclub-events-5-400x225.jpg" alt="">
                                <h3>titolo</h3>
                                <span>data</span>
                            </div>

                            <div class="col">
                                <img src="../../public/images/avada-nightclub-events-4-400x225.jpg" alt="">
                                <h3>titolo</h3>
                                <span>data</span>
                            </div>

                            <div class="col">
                                <img src="../../public/images/avada-nightclub-events-3-400x225.jpg" alt="">
                                <h3>titolo</h3>
                                <span>data</span>
                            </div>

                            <div class="col">
                                <img src="../../public/images/avada-nightclub-events-2-400x225.jpg" alt="">
                                <h3>titolo</h3>
                                <span>data</span>
                            </div>

                            <div class="col">
                                <img src="../../public/images/avada-nightclub-events-1-400x225.jpg" alt="">
                                <h3>titolo</h3>
                                <span>data</span>
                            </div>
                        </div>

                        <div class="col">
                            <button class="red-button">rsvp now</button>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <section class="vip">
            <div class="row justify-content-center align-items-center">
                <div class="col-lg-5">
                    <h4 class="blu-txt">SPECIAL GUEST DJ </h4>
                    <h2>esclusive vip lounge</h2>
                </div>
                <div class="col-lg-2">
                    <button class="red-button">
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

.theClub {
    background-image: url(../../public/images/avada-nightclub-cloud-background.jpg);
    background-size: cover;
    padding: 100px 0;
    color: gray;

    h4 {
        color: $primary-color;

    }



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
        right: 5%;
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

h2 {
    @include subtitle;
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
        padding: 0 -20px;
    }

    .info-button {
        position: absolute;
        top: 10%;
        left: 10%;
    }

}

.blu-button {
    @include blue-button;

}

.red-button {
    @include red-button;

}

.blu-txt {
    color: $primary-color;
}

.red-txt {
    color: $secondary-color;
}

.special-events {
    padding: 150px 0;
    background-image: url(../../public/images/avada-nightclub-homepage-events-background-new.jpg);
    background-size: cover;
    color: white;
}

.vip {
    background-image: url(../../public/images/avada-nightclub-vip-hero-new.jpg);
    background-size: cover;
    padding: 100px 0;
}
</style>
