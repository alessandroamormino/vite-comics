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
  gap: 1em 1.5em;

  width: calc(100% / 6 - 1.5em / 6 * 5);
  height: 280px;

  img {
    width: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    object-position: top;

    transition: transform .1s ease-in;
  }

  &:hover img {
    transform: scale(1.05)
  }

  .title {
    text-transform: uppercase;
  }
}
</style>