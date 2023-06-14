
<script >

export default {

    name: 'MainSpecialEvents',
    props: {
        details: Object,

    },

}
</script>

<template>
    <div class="col space">
        <img :src="details.img" alt="">
        <h3 class="red-txt">{{ details.text }}</h3>
        <span>{{ details.date }}</span>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;
</style>
