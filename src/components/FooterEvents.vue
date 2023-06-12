
<script >

export default {

    name: 'FooterEvents',
    props: {
        details: Object,

    }
}
</script>

<template>
    <!-- foto e paragrafo -->
    <div class="row space">
        <div class="col text-end">
            <!-- immagine -->
            <img :src="details.img" alt="">
        </div>
        <div class="col text-start">
            <!-- titolo piu span -->
            <h3>{{ details.text }}</h3>
            <span>{{ details.date }}</span>
        </div>
    </div>
</template>

<style lang="scss">
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;
</style>
