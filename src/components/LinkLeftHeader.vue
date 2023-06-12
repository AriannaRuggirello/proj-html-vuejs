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
    <nav>

        <a>{{ details.text }}</a>



    </nav>
</template>

<style lang="scss">
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;
</style>
