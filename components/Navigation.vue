<template>
    <div class="navigation">
        <ul class="list-none flex justify-between text-lg">
            <li class="mr-8 lg:mr-6">
                <nuxt-link to="/">
                    Home
                </nuxt-link>
            </li>
            <li class="mr-8 lg:mr-6">
                <a href="/CV_CarlBothamley.pdf" target="_blank">CV</a>
            </li>
            <li class="mr-8 lg:mr-6">
                <nuxt-link to="/about">
                    About
                </nuxt-link>
            </li>
            <li>
                <nuxt-link to="/contact">
                    Contact
                </nuxt-link>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'navigation'
    }
</script>

<style lang="scss" scoped>
    
    .navigation {
        max-width: 300px;
    }

    a {
        transition: .3s opacity ease;

        &:hover {
            opacity: .5;
        }
    }

    .nuxt-link-exact-active {
        @apply font-semibold;
        border-bottom: 2px solid currentColor;
    }
</style>