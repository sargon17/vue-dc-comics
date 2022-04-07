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
  props: ["thumb", "price", "series", "type"],
};
</script>

<style lang="scss" scoped>
.card {
  overflow: hidden;
  width: calc((100% / 12) * 2 - 20px);

  &__img-wrapper {
    width: 100%;
    aspect-ratio: 1;
    overflow: hidden;
  }

  &__content {
    max-width: 100%;

    .card__title {
      font-size: 0.8rem;
      font-weight: 500;
      margin: 10px 0;
      text-transform: uppercase;
    }
  }
}
</style>
