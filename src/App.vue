<template>
  <div id="app">
    <HeaderComponent />
    <MainContentSection :cardData="dcComics" />
    <DivisorBanner />
    <FooterSection />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainContentSection from "./components/MainContentSection.vue";
import DivisorBanner from "./components/DivisorBanner.vue";
import FooterSection from "./components/FooterSection.vue";

import dcComics from "@/data/dc-comics.json";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainContentSection,
    DivisorBanner,
    FooterSection,
  },
  data() {
    return {
      dcComics,
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Montserrat" serif;
}
</style>
