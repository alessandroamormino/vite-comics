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
    <div id="social">
        <div class="social-left">
            <button class="btn">Sign-up now!</button>
        </div>
        <div class="social-right">
            <a href="#">Follow us</a>
            <ul>

            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

#social {
    position: relative;
    z-index: 1;
    // position
    padding: 2em 0;
    background-color: $social-color;



}
</style>
