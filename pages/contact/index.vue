<template>
	<div>
		<page-headings
            heading="Contact"
            subHeading="Ring-a-ding-ding"
        />

        <p class="mb-4">If you want to request information about my services or just want to say hello then shoot me an email.</p>

        <p class="mb-6">
            <a class="text-xl font-semibold border-b-2 hover:border-b-0" href="mailto:carlbothamley@gmail.com">carlbothamley@gmail.com</a>
        </p>

        <p>I look forward to hearing from you.</p>
	</div>
</template>

<script>

    import PageHeadings from '~/components/PageHeadings';

	export default {
        components: {
            PageHeadings            
        }
    }
</script>
