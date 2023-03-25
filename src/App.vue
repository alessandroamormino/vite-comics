<script>
import AppNav from "./components/AppNav.vue";
import AppMain from "./components/AppMain.vue";
import AppBuy from "./components/AppBuy.vue";
export default {
  data() {
    return {

    }
  },
  components: {
    AppNav,
    AppMain,
    AppBuy,
  },
}
</script>
<template>
  <AppNav></AppNav>
  <AppMain></AppMain>
  <AppBuy></AppBuy>
</template>
<style lang="scss"></style>