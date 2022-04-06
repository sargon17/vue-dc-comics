<template>
  <div class="main">
    <div class="main-content">
      <h2>Conten goes here</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainContentSection",
};
</script>

<style lang="scss" scoped>
.main {
  width: 100%;
  height: 100px;
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
}
</style>
