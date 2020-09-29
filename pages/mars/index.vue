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
                videoSrc="https://www.youtube.com/embed/dMkZtgJxmvU"
            />
        </div>

        <p><a href="https://www.imdb.com/title/tt4939064/">https://www.imdb.com/title/tt4939064/</a></p>
        <p><a href="https://www.framestore.com/?language=en">https://www.framestore.com/?language=en</a></p>

	</div>
</template>

<script>

    import PageHeadings from '~/components/PageHeadings';
    import PageIntro from '~/components/PageIntro';
    import BodyCopy from '~/components/BodyCopy';
    import ResponsiveYouTube from '~/components/ResponsiveYouTube';
    import content from '~/content/pages/content.mars-page';

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
