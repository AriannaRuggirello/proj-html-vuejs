<script >


export default {
  name: 'PageHeader',

}





</script>

<template>
  <header>
    <div class="container text-center ">
      <div class="row align-items-center">
        <!-- nav bar con logo in centro -->
        <nav>

          <a href="#">HOME</a>
          <a href="#">THE CLUB</a>
          <a href="#">EVENTS</a>

          <a href="#">
            <img src="../../public/images/avada-nightclub-logo.png" alt="">
          </a>
          <a href="#">HOME</a>
          <a href="#">THE CLUB</a>
          <a href="#">EVENTS</a>
        </nav>

      </div>
      <!-- hero -->
      <div class="hero">

      </div>
    </div>


  </header>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;

header {
  background-image: url(../../public/images/avada-nightclub-home-hero.jpg);
  background-size: cover;
  height: 750px;
}

img {
  width: 200px;

}

a {
  color: white;
  font-weight: bold;
  padding-right: 40px;
  text-decoration: none;
}
</style>
