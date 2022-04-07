<template>
  <div class="main">
    <div class="jumbotron"></div>
    <div class="main-content">
      <div class="current-series" id="currentSeries">
        <div class="main-content-header">
          <h2>Current Series</h2>
        </div>
        <div class="main__cards-list">
          <ContentCard
            v-for="({ thumb, price, series, type }, index) in cardData"
            :key="'series' + index"
            :thumb="thumb"
            :price="price"
            :series="series"
            :type="type"
          />
        </div>
        <div class="main-content__btn-wrapper">
          <button>Load More</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ContentCard from "@/components/ContentCard.vue";

export default {
  name: "MainContentSection",
  components: {
    ContentCard,
  },
  props: ["cardData"],
};
</script>

<style lang="scss" scoped>
.main {
  width: 100%;
  background: #1c1c1c;
  color: white;

  .jumbotron {
    width: 100%;
    height: 42vh;
    background: url("@/assets/jumbotron.jpg") no-repeat;
    background-size: cover;
    position: relative;
  }

  &-content {
    max-width: 1200px;
    margin: 0 auto;
    position: relative;

    &-header {
      transform: translateY(-50%);
      background: #0282f9;
      position: absolute;
      top: 0;
      left: 0;
      padding: 5px 20px;
      h2 {
        font-size: 1.2rem;
        font-weight: 700;
        margin: 0;
        text-transform: uppercase;
      }
    }

    &__btn-wrapper {
      padding: 20px 20px;
      text-align: center;
      button {
        background: #0282f9;
        color: white;
        border: 1px solid #0282f9;
        padding: 0.5em 3em;
        font-size: 0.8rem;
        font-weight: 700;
        text-transform: uppercase;
        cursor: pointer;
        transition: all 0.3s ease;
        &:hover {
          background: #fff;
          color: #0282f9;
        }
      }
    }
  }

  &__cards-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    align-items: baseline;
    width: 100%;
    padding: 40px 0;
    gap: 10px;
  }
}
</style>
