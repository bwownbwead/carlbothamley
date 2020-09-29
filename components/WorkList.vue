<template>
	<div class="work-list">
		<nuxt-link
			v-for="item in content.workItems"
			:to="item.link"
			class="block mb-4 md:mb-6 lg:mb-8" 
		>
			<img 
				v-if="item.media.image.src && item.media.image.srcSet"
				:srcset="srcSetString(item.media.image.srcSet)"
				sizes="
					(min-width: 1200px) 800px,
					(min-width: 1024px) 666px,
            		100vw
            	"
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

		data() {
			return {
				content
			}
		},

		methods: {
			srcSetString(srcSetObj) {
				let string = '';

				for ( const key in srcSetObj) {
					string += `${srcSetObj[key]} ${key}w,`
				}

				return string;
			}
		}
	}
</script>

<style lang="scss" scoped>
	
</style>