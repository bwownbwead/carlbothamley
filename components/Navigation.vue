<template>
    <div>
        <ul>
            <li>
                <nuxt-link to="/">
                    Home
                </nuxt-link>
            </li>
            <li>
                <a href="/CV_CarlBothamley.pdf">CV</a>
            </li>
            <li>
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