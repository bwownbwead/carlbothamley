<template>
	<div class="site-wrap">
        <site-header />

        <div class="page-layout">
            <div class="side-bar">
                <side-bar 
                    :isHomePage="isHomePage"
                />
            </div>
            <div class="page-content lg:pt-10 xl:pt-20">
                <Nuxt />
            </div>
        </div>

        <footer class="mt-8 lg:hidden">
            <social-links />
        </footer>
	</div>
</template>

<script>
    import SiteHeader from '~/components/SiteHeader';
    import SideBar from '~/components/SideBar';

    export default {
        components: {
            SiteHeader,
            SideBar
        },

        computed: {
            isHomePage() {
                return this.$route.path === "/";
            }
        }
    }
</script>

<style lang="scss">
    html {
        @apply font-body;
    }

    body {
        @apply px-4 py-4;

        @screen sm {
            @apply px-6 py-6;
        }

        @screen md {
            @apply px-10 pt-12;
        }

        @screen lg {
            @apply pt-20;
        }

        @screen xl {
            @apply px-0;
        }
    }

    .site-wrap {
        max-width: 1080px;
        margin: 0 auto;
    }

    .page-layout {
        @screen lg {
            display: flex;
        }
    }

    .side-bar {
        flex-shrink: 0;

        @screen lg {
            width: 230px;
            margin-right: 50px;
        }

        @screen xl {
            width: 240px;
            margin-right: 100px;
        }
    }

    .page-content {
        @screen lg {
            flex-grow: 1;
        }
    }
</style>
