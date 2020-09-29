<template>
    <div>
        <page-headings
            :heading="content.heading"
            :subHeading="content.subHeading"
        />

        <page-intro
            v-if="content.intro"
            :intro="content.intro"
        />

        <!-- Carousel -->

        <body-copy
            :body="content.body"
        />

        <div class="my-8">
            <responsive-you-tube
                videoSrc="https://www.youtube.com/embed/iy4MrJrJNBk"
            />
        </div>

        <p><a href="https://www.taikoosugar.com/" target="_blank">https://www.taikoosugar.com/</a></p>
        <p><a href="https://www.swire.com/en/global/home.php" target="_blank">https://www.swire.com/en/global/home.php</a></p>

        <back-to-work-link />
    </div>
</template>

<script>

    import PageHeadings from '~/components/PageHeadings';
    import PageIntro from '~/components/PageIntro';
    import BodyCopy from '~/components/BodyCopy';
    import BackToWorkLink from '~/components/BackToWorkLink';
    import ResponsiveYouTube from '~/components/ResponsiveYouTube';
    import content from '~/content/pages/content.swire-page';

    export default {
        components: {
            PageHeadings,
            PageIntro,
            BodyCopy,
            ResponsiveYouTube
        },

        data() {
            return {
                content
            }
        }
    }
</script>
