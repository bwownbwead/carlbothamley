<template>
    <div class="navigation">
        <ul class="list-none flex justify-between text-lg">
            <li class="mr-8 lg:mr-6">
                <nuxt-link to="/">
                    Home
                </nuxt-link>
            </li>
            <li class="mr-8 lg:mr-6">
                <a href="/CVupdating.pdf" target="_blank">CV</a>
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
        border-bottom: 2px solid transparent;
        transition: .3s border-color ease;

        &:hover {
            border-bottom: 2px solid currentColor;
        }
    }

    .nuxt-link-exact-active {
        @apply font-semibold;
        border-bottom: 2px solid currentColor;
    }
</style>
