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
    <div class="container text-center ">
      <nav>

        <LinkLeftHeader v-for="link in linksLeft" :href="link.url" :details="link" :class="link.active ? 'active' : ''" />

        <a href="#">
          <img src="../../public/images/avada-nightclub-logo.png" alt="">
        </a>


        <LinkRightHeader v-for="link in linksRight" :href="link.url" :details="link"
          :class="link.active ? 'active' : ''" />
      </nav>
      <!-- hero -->
      <div class="hero">
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
        <!-- immagine,testo e pulsante -->
        <div class="row row-cols-1">
          <div class="col">
            <img src="../../public/images/avada-nightclub-homepage-image-800x398.png" alt="">
            <h2> making memories all night long </h2>
            <button>BECOME A VIP</button>
            <!-- play showreel img -->
            <div class="col">
              <img src="../../public/images/avada-nightclub-play-showreel-200x47.png" alt="">

            </div>
          </div>
        </div>
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



  nav {
    img {
      width: 200px;


    }

    a {
      color: white;
      font-weight: bold;
      padding-right: 40px;
      text-decoration: none;
    }

    .active {
      color: $secondary-color;
      border-bottom: 2px solid $secondary-color;
    }
  }

  .hero {


    img {
      border-bottom: 3px solid $primary-color;
      margin-bottom: 20px;
    }

    button {
      @include red-button
    }

    .icon {
      width: 70px;
      height: 70px;
      background-color: white;
      color: grey;
      border-radius: 5px;
      padding: 10px;
      margin-bottom: 10px;


      .fa-folder {
        font-size: 30px;
      }

      h3 {
        color: #65bc7b;
        font-size: 30px;
      }

      h4 {
        font-weight: bold;
        font-size: small;
      }
    }


  }
}
</style>
