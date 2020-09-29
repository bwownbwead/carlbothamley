<template>
	<div class="work-list">
		<nuxt-link
			v-for="item in content.workItems"
			:to="item.link"
			class="block mb-4 md:mb-6 lg:mb-8" 
		>
			<img 
				:src="item.media.image.src"
				:alt="item.area"
				class="mb-1 lg:mb-2"
			>

			<p>
				<span class="font-semibold text-lg">_{{ item.area }}</span>_{{ item.type }}
			</p>
		</nuxt-link>
	</div>
</template>

<script>
	import content from '~/content/content.work-list';

	export default {
		name: 'work-list',

		components: {
			
		},

		data() {
			return {
				content
			}
		}
	}
</script>

<style lang="scss" scoped>
	
</style>