<template>
  <div id="app">
    <HeaderComponent />
    <MainContentSection />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainContentSection from "./components/MainContentSection.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainContentSection,
  },
};
</script>

<style lang="scss">
#app {
  font-family: "Montserrat" serif;
}
</style>
