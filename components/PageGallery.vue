<template>
    <silent-box 
        :gallery="modalImages"
        class="item silentbox-gallery block mb-4 md:mb-6 lg:mb-8"
    >
        <img 
            :src="galleryImage"
            class="mb-1 lg:mb-2"
        >

        <p class="page-gallery-text text-white absolute bottom-0 left-0 p-3 md:p-5 lg:p-6 uppercase">
            <svg xmlns="http://www.w3.org/2000/svg" overflow="visible" viewBox="0 0 284.97 237.95"><g><path d="M265.63 34.72h-11.38V19.34C254.25 8.68 245.58 0 234.91 0H19.34C8.68 0 0 8.68 0 19.34v168.54c0 10.66 8.68 19.34 19.34 19.34H35.7v11.39c0 10.66 8.68 19.34 19.34 19.34h210.59c10.66 0 19.34-8.68 19.34-19.34V54.06c0-10.66-8.68-19.34-19.34-19.34zM35.7 54.06v137.16H19.34c-1.81 0-3.34-1.53-3.34-3.34V19.34c0-1.81 1.53-3.34 3.34-3.34h215.57c1.81 0 3.34 1.53 3.34 3.34v15.39H55.04C44.38 34.72 35.7 43.4 35.7 54.06zm233.27 164.55c0 1.81-1.53 3.34-3.34 3.34H55.04c-1.81 0-3.34-1.53-3.34-3.34V54.06c0-1.81 1.53-3.34 3.34-3.34h210.59c1.81 0 3.34 1.53 3.34 3.34v164.55z"/><circle cx="92.5" cy="93.67" r="27.08"/><path d="M198.39 91.1l-68.03 66.53-20.74-20.3-42.71 42.74.07 25.26h187.28l-.37-59.45z"/></g></svg>
        </p>
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
            }

            .page-gallery-text {
                transform: scale(1.25);
            }
        }
    }

    .page-gallery-text {
        svg {
            fill: #fff;
            width: 25px;
        }
    }

</style>