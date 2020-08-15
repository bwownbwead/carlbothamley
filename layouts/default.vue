<template>
	<div class="site-wrap">
        <div class="mb-6">
            <navigation />
        </div>
		<Nuxt />
	</div>
</template>

<script>
    import Navigation from '~/components/Navigation';

    export default {
        components: {
            Navigation
        }
    }
</script>

<style lang="scss">
    html {
        font-family: 'Source Sans Pro', sans-serif;
    }

    .site-wrap {
        max-width: 1070px;
        margin: 0 auto;
    }
</style>
