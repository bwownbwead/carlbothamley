<template>
    <silent-box 
        :gallery="modalImages"
        class="item silentbox-gallery block mb-4 md:mb-6 lg:mb-8"
    >
        <img 
            :src="galleryImage"
            class="mb-1 lg:mb-2"
        >

        <p class="page-gallery-text text-white absolute bottom-0 left-0 p-3 md:p-5 lg:p-6 uppercase">Open gallery_</p>
    </silent-box>
</template>

<script>
    export default {
        name: 'page-gallery',

        props: {
            modalImages: {
                type: Array,
                default: () => []
            },

            galleryImage: {
                type: String,
                default: () => ""
            }
        }
    }
</script>

<style lang="scss" scoped>

    
    .item {

        > img {
            transition: .3s all ease;
            background-color: #000;
        }

        .page-gallery-text {
            transition: .3s all ease;
        }

        &:hover {

            > img {
                transform: scale(1.01);
                // opacity: .5;
            }

            .page-gallery-text {
                transform: scale(1.01);
                font-size: 20px;
            }
        }
    }

</style>