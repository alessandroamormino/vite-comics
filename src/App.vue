<script>
import AppNav from "./components/AppNav.vue";
import AppMain from "./components/AppMain.vue";
import AppBuy from "./components/AppBuy.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  data() {
    return {

    }
  },
  components: {
    AppNav,
    AppMain,
    AppBuy,
    AppFooter
  },
}
</script>
<template>
  <AppNav></AppNav>
  <AppMain></AppMain>
  <AppBuy></AppBuy>
  <AppFooter></AppFooter>
</template>
<style lang="scss"></style>