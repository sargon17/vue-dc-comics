<template>
  <div class="card">
    <div class="card__img-wrapper">
      <img :src="thumb" :alt="series + type + price" />
      <div class="card__img-content">
        <h3 class="card__img-content__title">{{ series }}</h3>
        <p class="card__img-content__subtitle">{{ type }}</p>
        <p class="card__img-content__price">{{ price }}</p>
      </div>
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

  &:hover {
    .card__img-content {
      transform: translateY(-100%);
    }
    .card__title {
      transform: translateY(-200%);
    }
  }

  &__img-wrapper {
    width: 100%;
    aspect-ratio: 1;
    overflow: hidden;
    position: relative;
    border-radius: 4px;
    z-index: 1;

    .card__img-content {
      position: absolute;
      top: 100%;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(
        360deg,
        #1c1c1c 10%,
        rgba(28, 28, 28, 0.098) 100%
      );
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-items: flex-start;
      transition: all 0.3s ease-out;
      transition-delay: 100ms;
      cursor: pointer;
      &__title {
        max-width: 100%;
        font-size: 1rem;
        font-weight: 700;
        margin: 2px 5px;
        text-transform: uppercase;
        word-break: break-word;
      }
      &__subtitle {
        font-size: 0.6rem;
        font-weight: 400;
        margin: 2px 5px;
        text-transform: uppercase;
      }
      &__price {
        font-size: 0.8rem;
        font-weight: 700;
        margin: 2px 5px;
        color: #0282f9;
        text-transform: uppercase;
      }
    }
  }

  &__content {
    max-width: 100%;

    .card__title {
      font-size: 0.8rem;
      font-weight: 500;
      margin: 10px 0;
      text-transform: uppercase;
      transition: all 0.3s ease-out;
      transition-delay: 100ms;
    }
  }
}
</style>
