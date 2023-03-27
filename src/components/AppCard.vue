<script>
export default {
  data() {
    return {}
  },
  props: {
    img: String,
    title: String,
  }
}
</script>
<template>
  <div class="card">
    <img :src="img" :alt="title">
    <span class="title">{{ title }}</span>
  </div>
</template>
<style lang="scss" scoped>
.card {
  display: flex;
  flex-flow: column nowrap;

  width: calc(100% / 6 - 1.5em / 6 * 5);
  height: 280px;

  img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    object-position: top;
  }

  .title {
    padding: 1em 0;
    text-transform: uppercase;
  }
}
</style>