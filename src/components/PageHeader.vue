<script >

import LinkLeftHeader from '../components/LinkLeftHeader.vue';
import LinkRightHeader from '../components/LinkRightHeader.vue';



export default {
  name: 'PageHeader',
  components: {
    LinkLeftHeader,
    LinkRightHeader,
  },
  data() {
    return {
      linksLeft: [
        {
          text: 'HOME',
          url: '#',
          active: true

        },

        {
          text: 'THE CLUB',
          url: '#',
          active: false

        },

        {
          text: 'EVENTS',
          url: '#',
          active: false

        },
      ],
      linksRight: [
        {
          text: 'JOBS',
          url: '#',
          active: false

        },

        {
          text: 'NEWS',
          url: '#',
          active: false

        },

        {
          text: 'CONTACT US',
          url: '#',
          active: false

        },
      ]



    }
  }
}
</script>

<template>
  <header>
    <!-- overlay scuro sull'immagine -->
    <div class="overlay">
      <div class="container text-center">
        <!-- menu di navigazione -->
        <nav>
          <!-- voci di menu sx -->
          <LinkLeftHeader v-for="link in linksLeft" :href="link.url" :details="link"
            :class="link.active ? 'active' : ''" />

          <!-- logo img -->

          <img src="../../public/images/avada-nightclub-logo.png" alt="">


          <!-- voci di menu dx -->
          <LinkRightHeader v-for="link in linksRight" :href="link.url" :details="link"
            :class="link.active ? 'active' : ''" />
        </nav>

        <!-- hero -->
        <section class="hero">
          <!-- row con icone alla fine -->
          <div class="row justify-content-end ">

            <!-- icon nella parte dx -->
            <div class="icon">
              <i class="fa-solid fa-folder"></i>
              <h4>Demos</h4>

            </div>
          </div>
          <div class="row justify-content-end ">
            <div class="icon">
              <h3><sup>$</sup>39</h3>
              <h4>On Sale</h4>
            </div>

          </div>

          <!-- immagine,testo e pulsante centrali-->
          <div class="row row-cols-1">
            <div class="col">
              <img class="hero-img" src="../../public/images/avada-nightclub-homepage-image-800x398.png" alt="">
              <h2> making memories all night long </h2>
              <button>BECOME A VIP</button>
              <!-- play showreel img -->
              <div class="col">

                <img src="../../public/images/avada-nightclub-play-showreel-200x47.png" alt="">

              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;

header {
  color: white;
  background-image: url(../../public/images/avada-nightclub-home-hero.jpg);
  background-size: cover;
  position: relative;



  nav {


    img {
      width: 200px;
    }

    a {
      width: 50%;
      margin: 0 50px;
      color: white;
      font-weight: bold;
      // padding: 0 40px 0 40px;
      text-decoration: none;


      &.active,
      &:hover {

        color: $secondary-color;
        border-bottom: 2px solid $secondary-color;
      }
    }


  }

  .hero {
    padding-bottom: 50px;

    .hero-img {
      border-bottom: 3px solid $primary-color;
      margin-bottom: 20px;
    }

    button {
      background-color: $secondary-color;
      margin: 30px 0
    }

    button:hover {
      background-color: #f51265;
    }

    .icon {
      width: 70px;
      height: 70px;
      background-color: white;
      color: grey;
      border-radius: 5px;
      padding: 10px;
      margin-bottom: 10px;
      position: relative;


      .fa-folder {
        font-size: 30px;
        position: absolute;
        left: 30%;
        top: 15%;
      }

      h3 {
        color: #65bc7b;
        font-size: 30px;
        font-weight: bold;
      }

      h4 {
        font-weight: bold;
        font-size: small;
        position: absolute;
        top: 60%;
      }
    }


  }
}
</style>
