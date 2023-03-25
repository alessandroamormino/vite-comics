<script>
export default {
    data() {
        return {
            lists: [
                [
                    {
                        title: 'Dc Comics',
                        links: [
                            'Characters',
                            'Comics',
                            'Movies',
                            'TV',
                            'Games',
                            'Videos',
                            'News',
                        ],
                    },
                    {
                        title: 'Shop',
                        links: [
                            'Shop DC',
                            'Shop DC Collectibles',
                        ],
                    },
                ],
                [
                    {
                        title: 'DC',
                        links: [
                            'Terms Of Use',
                            'Privacy policy (New)',
                            'Ad Choices',
                            'Advertising',
                            'Jobs',
                            'Subscriptions',
                            'Talent Workshops',
                            'CPSC Certificates',
                            'Ratings',
                            'Shop Help',
                            'Contact Us',
                        ],
                    },
                    {
                        title: 'Sites',
                        links: [
                            'DC',
                            'MAD Magazine',
                            'DC Kids',
                            'DC Universe',
                            'DC Power Visa',
                        ],
                    },
                ],
            ],
        }
    },
}
</script>
<template>
    <footer>
        <div class="container-centered">
            <div class="footer-flex">
                <div class="list-container">
                    <div class="list-column">
                        <div v-for="(list) in lists[0]" class="list">
                            <h2>{{ list.title }}</h2>
                            <ul>
                                <li v-for="link in list.links">
                                    <a href="#">{{ link }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div v-for="(list) in lists[1]" class="list">
                        <h2>{{ list.title }}</h2>
                        <ul>
                            <li v-for="link in list.links">
                                <a href="#">{{ link }}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="logo-bg">
                    <img src="/img/dc-logo-bg.png" alt="dc-logo">
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

footer {
    background-image: url('/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;

    padding: 2em 0;

    .footer-flex {
        display: flex;
        justify-content: space-between;

        position: relative;
    }

    .list-container {
        display: flex;
        gap: 2em;

        flex-grow: 1;
    }

    .list-column {
        display: flex;
        flex-flow: column nowrap;

    }

    .list {
        color: #fff;

        h2 {
            margin: .5em 0;
            text-transform: uppercase;
        }
    }

    @include links(rgb(157, 157, 157));

    a {
        text-transform: capitalize;
        font-family: Arial, Helvetica, sans-serif;
        font-size: .9em;
    }

    .logo-bg {
        position: absolute;
        right: 0;
        top: -40%;
    }

}
</style>