<template>
    <div class="social-links border-t-4 pt-4 border-almostblack">
        <ul class="flex">
            <li
                v-for="social in content.socialLinks"
                class="mr-4"
            >
                <a 
                    :key="social.platform"
                    :href="social.url"
                >
                    <img :src="social.icon" :alt="social.platform">
                </a>
            </li>
        </ul>
    </div>
</template>

<script>

    import content from '~/content/content.social-links';

    export default {
        name: 'social-links',

        data() {
            return {
                content
            }
        }
    }
</script>

<style lang="scss" scoped>
    
    li {
        max-width: 30px;

        @screen lg {
            max-width: 20px;            
        }
    }
    
</style>