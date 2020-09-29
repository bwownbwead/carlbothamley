<template>
    <div class="mb-8">
        <h1 
            v-if="heading"
            class="text-2xl font-semibold"
        >
            {{ heading }}
        </h1>
        <h2 v-if="subHeading">
            {{ subHeading }}_
        </h2>
    </div>
</template>

<script>
    export default {
        name: 'page-headings',

        props: {
            heading: {
                type: String,
                default: () => ""
            },

            subHeading: {
                type: String,
                default: () => ""
            }
        }
    }
</script>