<template>
    <div class='embed-container'>
        svsadvsd
        <iframe 
            :src="videoSrc"
            frameborder='0' 
            allowfullscreen
        ></iframe>
    </div>
</template>

<script>
    export default {
        name: 'responsive-you-tube',

        props: {
            videoSrc: {
                type: String,
                default: () => ""
            }
        }
    }
</script>

<style lang="scss">
    .embed-container { 
        position: relative; 
        padding-bottom: 56.25%; 
        height: 0; 
        overflow: 
        hidden; 
        max-width: 100%; 

        iframe, object, embed {
            position: absolute; 
            top: 0; 
            left: 0; 
            width: 100%; 
            height: 100%;
        }
    }
</style>