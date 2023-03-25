<script>
export default {
    data() {
        return {
            icons: [
                '/img/footer-facebook.png',
                '/img/footer-twitter.png',
                '/img/footer-youtube.png',
                '/img/footer-pinterest.png',
                '/img/footer-periscope.png',
            ],
        }
    },
}
</script>
<template>
    <footer>
        <div class="container-centered">
            <div class="flex-container">
                <div class="social-left">
                    <button class="btn">Sign-up now!</button>
                </div>
                <div class="social-right">
                    <a href="#">Follow us</a>
                    <ul>
                        <li v-for="icon in icons">
                            <a href="#">
                                <img :src="icon" alt="social">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

footer {
    position: relative;
    z-index: 1;
    // position
    padding: 2em 0;
    background-color: $footer-color;

    .flex-container {
        @include flexSpaceBetween();
        @include links($main-color);

        .social-left {
            .btn {
                padding: .5em 1em;
                border: 1.5px solid $main-color;
                background-color: $footer-color;
                color: #fff;
                text-transform: uppercase;
                font-size: 1em;
            }
        }

        .social-right {
            @include flexSpaceCenter();
            gap: 1.5em;

            ul {
                @include flexSpaceCenter();
                gap: 1em;

                li {
                    img {
                        width: 30px;
                    }
                }

            }

        }


    }

}
</style>
