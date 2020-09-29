<template>
    <h3 
        class="text-xl font-semibold mb-6 lg:pr-10"
    >
        {{ intro }}
    </h3>
</template>

<script>
    export default {
        name: 'page-intro',

        props: {
            intro: {
                type: String,
                default: () => ""
            }
        }
    }
</script>