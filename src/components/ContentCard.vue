<template>
  <div class="card">
    <div class="card__img-wrapper">
      <img :src="thumb" :alt="series + type + price" />
    </div>
    <div class="card__content">
      <h3 class="card__title">{{ series }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContentCard",
  props: {
    thumb: String,
    price: String,
    series: String,
    type: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  overflow: hidden;

  &__img-wrapper {
    width: 100%;
    aspect-ratio: 1;
    background: #1c1c1c;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }
}
</style>
