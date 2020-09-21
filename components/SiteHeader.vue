<template>
    <div class="
        site-header
        mb-6
        items-baseline
        justify-between
        sm:flex
    ">
        <logo-block />
        <navigation />
    </div>
</template>

<script>
    import Navigation from '~/components/Navigation';
    import LogoBlock from '~/components/LogoBlock';

    export default {
        name: 'site-header',

        components: {
            Navigation,
            LogoBlock
        }
    }
</script>

<style lang="scss" scoped>
    .site-header {
        
    }
</style>