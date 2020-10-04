<template>
    <div>
        <h2 
            v-html="content.heading"
            class="text-3xl leading-8 mb-5"
        />
        <p class="mb-8 max-w-md lg:max-w-none">
            {{ content.body }}
        </p>

        <div class="hidden lg:block">
            <social-links />
        </div>
    </div>
</template>

<script>
    import content from '~/content/content.sidebar';
    import SocialLinks from '~/components/SocialLinks';

    export default {
        name: 'side-bar',

        components: {
            SocialLinks
        },

        data() {
            return {
                content
            }
        }
    }
</script>