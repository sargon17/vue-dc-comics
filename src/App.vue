<template>
  <div id="app">
    <HeaderComponent />
    <MainContentSection />
    <DivisorBanner />
    <FooterSection />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainContentSection from "./components/MainContentSection.vue";
import DivisorBanner from "./components/DivisorBanner.vue";
import FooterSection from "./components/FooterSection.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainContentSection,
    DivisorBanner,
    FooterSection,
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Montserrat" serif;
}
</style>
