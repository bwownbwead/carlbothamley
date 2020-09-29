<template>
    <div class="
        site-header
        mb-10
        items-baseline
        justify-between
        sm:flex
        lg:mb-6
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