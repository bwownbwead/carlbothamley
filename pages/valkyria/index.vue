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
                videoSrc="https://www.youtube.com/embed/E3iMSvMYcvA"
            />
        </div>

        <p><a href="https://www.liseberg.com/valkyria/" target="_blank">https://www.liseberg.com/valkyria/</a></p>
        <p><a href="https://www.youtube.com/user/Cyaarl/videos" target="_blank">https://www.youtube.com/user/Cyaarl/videos</a></p>

        <back-to-work-link />
    </div>
</template>

<script>

    import PageHeadings from '~/components/PageHeadings';
    import PageIntro from '~/components/PageIntro';
    import BodyCopy from '~/components/BodyCopy';
    import BackToWorkLink from '~/components/BackToWorkLink';
    import ResponsiveYouTube from '~/components/ResponsiveYouTube';
    import content from '~/content/pages/content.valkyria-page';

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
