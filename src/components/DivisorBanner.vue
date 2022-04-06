<template>
  <div class="banner">
    <div class="banner-content">
      <div
        class="banner-card"
        v-for="{ id, title, img, alt } in bannerData"
        :key="id"
      >
        <div class="banner-card__img-container">
          <img :src="img" :alt="alt" />
        </div>
        <p>{{ title }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import bannerData from "../data/bannerData.js";

export default {
  name: "DivisorBanner",
  data() {
    return {
      bannerData,
    };
  },
  methods: {
    imgPath(img) {
      return `../assets/${img}`;
    },
  },
};
</script>

<style lang="scss" scoped>
.banner {
  height: 20vh;
  width: 100%;
  background: #0282f9;
  &-content {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    height: 100%;
  }
  &-card {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;

    &__img-container {
      height: 48px;
      aspect-ratio: 1;
      display: flex;
      justify-content: flex-end;
      align-items: center;

      img {
        max-width: 100%;
        max-height: 100%;
      }
    }
    p {
      text-transform: uppercase;
      font-size: 0.8rem;
      font-weight: 600;
      color: #fff;
    }
  }
}
</style>
