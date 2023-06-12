<script >

export default {

    name: 'LinkLeftHeader',
    props: {
        details: Object,

    }
}
</script>

<template>
    <!-- nav bar con logo in centro -->



    <a>{{ details.text }}</a>
</template>

<style lang="scss">
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;
</style>
