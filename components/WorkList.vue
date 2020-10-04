<template>
	<div class="work-list">
		<div 
			v-for="item in content.workItems"
			class="relative" 
		>
			<nuxt-link
				v-if="item.link"
				:to="item.link"
				class="item block mb-4 md:mb-6 lg:mb-8"
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

			<silent-box 
				v-else
				:gallery="item.modalImages"
				class="item silentbox-gallery block mb-4 md:mb-6 lg:mb-8"
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
			</silent-box>
		</div>
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

<style lang="scss">
	
	.work-list {

		.item {
			> img {
				transition: .3s all ease;
			}

			&:hover {
				> img {
					opacity: .8;
					transform: scale(1.01);
				}
			}
		}
	}

</style>