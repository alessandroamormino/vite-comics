<script>
export default {
    data() {
        return {
            icons: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    title: 'Digital Comics'
                },
                {
                    image: '/img/buy-comics-merchandise.png',
                    title: 'DC Merchandise'
                },
                {
                    image: '/img/buy-comics-subscriptions.png',
                    title: 'Subscription'
                },
                {
                    image: '/img/buy-comics-shop-locator.png',
                    title: 'Comic Shop Locator'
                },
                {
                    image: '/img/buy-dc-power-visa.svg',
                    title: 'DC Power Visa'
                },
            ],
        }
    },
}
</script>
<template>
    <div id="buy">
        <div class="container-centered">
            <ul>
                <li v-for="icon in icons">
                    <a href="#">
                        <img :src="icon.image" :alt="icon.title">
                        {{ icon.title }}
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

#buy {
    position: relative;
    z-index: 1;

    background-color: $main-color;
    padding: 3em 0;

    color: #fff;

    ul {
        @include flexSpaceBetween();

        li {

            @include links(#fff);

            a {
                @include flexSpaceCenter();
                gap: .5em;

                img {
                    height: 50px;
                    width: 50px;
                    object-fit: contain;
                }
            }
        }
    }
}
</style>