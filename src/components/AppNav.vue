<script>
export default {
    data() {
        return {
            links: [
                'Characters',
                'Comics',
                'Movies',
                'Tv',
                'Games',
                'Collectibles',
                'Videos',
                'Fans',
                'News',
                'Shop'
            ],
        }
    },
}
</script>
<template>
    <nav>
        <div class="container-centered">
            <div class="nav-left">
                <a href="#">
                    <img src="/img/dc-logo.png" alt="Logo">
                </a>
            </div>
            <div class="nav-right">
                <ul>
                    <li v-for="link in links"><a href="#">{{ link }}</a></li>
                </ul>
            </div>
        </div>
    </nav>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

nav {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;

    z-index: 2;

    width: 100%;

    background-color: #fff;

    .container-centered {


        // position
        display: flex;
        justify-content: space-between;
        align-items: center;
        // flex

        .nav-left {
            img {
                width: 75%;
            }
        }

        .nav-right {
            ul {
                display: flex;
                justify-content: center;
                align-items: center;
                gap: 2em;

                li {
                    padding: 3em 0;
                }
            }

            @include links(#000);

            a {
                position: relative;

                padding: 3em 0;

                &:hover {
                    color: $main-color;

                    &::after {
                        content: '';

                        position: absolute;
                        bottom: 0;
                        right: 0;
                        left: 0;

                        width: 100%;
                        height: 4px;


                        background-color: $main-color;
                    }
                }
            }
        }
    }

}
</style>