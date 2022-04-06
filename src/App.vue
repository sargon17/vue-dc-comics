<template>
  <div id="app">
    <HeaderComponent />
    <MainContentSection />
    <DivisorBanner />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainContentSection from "./components/MainContentSection.vue";
import DivisorBanner from "./components/DivisorBanner.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainContentSection,
    DivisorBanner,
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Montserrat" serif;
}
</style>
