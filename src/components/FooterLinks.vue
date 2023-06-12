
<script >

export default {

    name: 'FooterLinks',
    props: {
        details: Object,

    }
}
</script>

<template>
    <li>
        <a>{{ details.text }}</a>
    </li>
</template>

<style lang="scss">
@use '../style/partials/variables.scss' as *;
@use '../style/partials/mixin.scss' as *;
</style>
