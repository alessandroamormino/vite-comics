<script>
import AppNav from "./components/AppNav.vue";
import AppMain from "./components/AppMain.vue";
import AppBuy from "./components/AppBuy.vue";
import AppLinks from "./components/AppLinks.vue";
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
    AppLinks,
    AppFooter
  },
}
</script>
<template>
  <AppNav></AppNav>
  <AppMain></AppMain>
  <AppBuy></AppBuy>
  <AppLinks></AppLinks>
  <AppFooter></AppFooter>
</template>
<style lang="scss"></style>