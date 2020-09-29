<template>
    <div>
        <p
             v-for="line in body"
        >
            {{ line }}
        </p>
    </div>
</template>

<script>
    export default {
        name: 'body-copy',

        props: {
            body: {
                type: Array,
                default: () => []
            }
        }
    }
</script>

<style lang="scss" scoped>
    p + p {
        @apply my-6;
    }
</style>