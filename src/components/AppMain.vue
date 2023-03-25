<script>
export default {
    data() {
        return {

        }
    },
}
</script>
<template>
    <div id="main">
        <div class="container-centered">
            <h2>Content goes here</h2>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../scss/variables.scss' as *;

#main {
    padding: 3em 0;
    background-color: $content-color;
    color: #fff;
}
</style>