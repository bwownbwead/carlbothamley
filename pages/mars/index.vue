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

        <page-gallery
            :modalImages="content.modalImages"
            :galleryImage="content.galleryImage"
        />

        <body-copy
            :body="content.body"
        />

        <div class="my-8">
            <responsive-you-tube
                videoSrc="https://www.youtube.com/embed/dMkZtgJxmvU"
            />
        </div>

        <p><a href="https://www.imdb.com/title/tt4939064/" target="_blank">https://www.imdb.com/title/tt4939064/</a></p>
        <p><a href="https://www.framestore.com/?language=en" target="_blank">https://www.framestore.com/?language=en</a></p>

        <back-to-work-link />
	</div>
</template>

<script>

    import PageHeadings from '~/components/PageHeadings';
    import PageGallery from '~/components/PageGallery';
    import PageIntro from '~/components/PageIntro';
    import BodyCopy from '~/components/BodyCopy';
    import BackToWorkLink from '~/components/BackToWorkLink';
    import ResponsiveYouTube from '~/components/ResponsiveYouTube';
    import content from '~/content/pages/content.mars-page';

	export default {
        components: {
            PageHeadings,
            PageGallery,
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
