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

        <h3 
            v-if="content.intro"
            class="text-xl font-semibold mb-6 lg:pr-10"
        >
            {{ content.intro }}
        </h3>

        <body-copy
            :body="content.body"
        />
	</div>
</template>

<script>

    import PageHeadings from '~/components/PageHeadings';
    import BodyCopy from '~/components/BodyCopy';
    import content from '~/content/pages/content.about-page';

	export default {
        components: {
            PageHeadings,
            BodyCopy
        },

        data() {
            return {
                content
            }
        }
    }
</script>
