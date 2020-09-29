<template>
	<div>
		<page-headings
            :heading="content.heading"
            :subHeading="content.subHeading"
        />

        <img 
            :src="content.image"
            alt="Carl Bothamley"
            class="max-w-xs mb-8" 
        >

        <page-intro
            v-if="content.intro"
            :intro="content.intro"
        />

        <body-copy
            :body="content.body"
        />
	</div>
</template>

<script>

    import PageHeadings from '~/components/PageHeadings';
    import PageIntro from '~/components/PageIntro';
    import BodyCopy from '~/components/BodyCopy';
    import content from '~/content/pages/content.about-page';

	export default {
        components: {
            PageHeadings,
            PageIntro,
            BodyCopy
        },

        data() {
            return {
                content
            }
        }
    }
</script>
