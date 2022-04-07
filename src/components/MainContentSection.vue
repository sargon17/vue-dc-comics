<template>
  <div class="main">
    <div class="main-content">
      <div class="main__cards-list">
        <ContentCard
          v-for="({ thumb, price, series, type }, index) in cardData"
          :key="'series' + index"
          :thumb="thumb"
          :price="price"
          :series="series"
          :type="type"
          class="card"
        />
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
  props: {
    cardData: Array,
  },
};
</script>

<style lang="scss" scoped>
.main {
  width: 100%;
  background: #1c1c1c;
  color: white;

  &-content {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
  }

  &__cards-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    padding: 0 20px;

    card {
      width: 100% / 3;
      margin: 20px;
    }
  }
}
</style>
