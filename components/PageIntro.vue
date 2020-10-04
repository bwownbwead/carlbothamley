<template>
    <h3 
        class="text-xl font-semibold mb-6 lg:mb-10 lg:pr-10 leading-tight"
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