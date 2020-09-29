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
                    <span v-html="social.icon" />
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
        a, span {
            display: inline-block;
        }

        ::v-deep svg {
            @apply w-5;
        }
    }
    
</style>