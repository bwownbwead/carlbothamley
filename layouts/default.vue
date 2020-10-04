<template>
	<div class="site-wrap">
        <site-header />

        <div class="page-layout">
            <transition name="fade">
                <div 
                    v-if="isHomePage || isDesktop"
                    class="side-bar"
                >
                    <side-bar />
                </div>
            </transition>
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

        data() {
            return {
                isDesktop: false
            }
        },

        computed: {
            isHomePage() {
                return this.$route.path === "/";
            }
        },

        mounted() {
            this.checkForDesktop();
            window.addEventListener('resize', this.checkForDesktop);
        },

        methods: {
            checkForDesktop() {
                this.isDesktop = window.matchMedia('(min-width: 1024px)').matches;
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
        position: relative;
        
        @screen lg {
            flex-grow: 1;
        }
    }

    .page-enter-active,
    .page-leave-active {
        transition-property: opacity;
        transition-timing-function: ease-in-out;
        transition-duration: 250ms;
    }
    .page-enter,
    .page-leave-to {
        opacity: 0;
    }

    .fade-enter-active, .fade-leave-active {
        transition: opacity .25s ease-in-out;
    }

    .fade-enter, .fade-leave-to {
        opacity: 0;
    }

    .site-wrap {
        .silentbox-item {
            width: 100%;
            background: transparent;
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;

            > img {
                opacity: 0 !important;
            }
        }

        #silentbox-overlay__background {
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: none;
        }

        #silentbox-overlay__arrow-buttons .arrow {
            border-left: 2px solid #000;
            border-top: 2px solid #000;
            pointer-events: auto;

            &:hover,
            &:focus {
                border-color: #000;
                animation-name: none;
            }
        }

        #silentbox-overlay {
            pointer-events: auto;
        }

        #silentbox-overlay__embed {
            img,
            iframe {
                background-color: #fff;
                box-shadow: none;
            }
        }

        #silentbox-overlay__close-button {
            pointer-events: auto;

            &:hover {
                background-color: rgba(0, 0, 0, 0.2);
            }

            .icon {
                &:before,
                &:after {
                    background: #000;
                }

                &:hover {
                    &:before,
                    &:after {
                        background: #000;
                        left: 5%;
                        width: 100%;
                    }                   
                }
            }
        }

        .silentbox-gallery {
            position: relative;

            > div {
                pointer-events: none;

                &:nth-of-type(1) {
                    pointer-events: auto;
                }
            }
        }
    }
</style>
