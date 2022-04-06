<template>
  <div>
    <header class="header">
      <div class="header--content">
        <div class="header__logo-wrapper">
          <img src="../assets/dc-logo.png" alt="dc logo" />
        </div>
        <nav class="header__nav">
          <ul class="header__nav-list">
            <li
              v-for="{ title, id } in navigationData"
              :key="id"
              class="header__nav-item"
            >
              <a href="#" class="header__nav-link">
                <span class="header__nav-link-text">{{ title }}</span>
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
  </div>
</template>

<script>
import navigationData from "../data/navigationData.js";

export default {
  name: "HeaderComponent",
  data() {
    return {
      navigationData,
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 100px;
  background: #ffffff;

  &--content {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
  }

  &__nav {
    &-list {
      display: flex;
      align-items: center;
      list-style: none;
    }
    &-item {
      &:not(:last-child) {
        margin-right: 20px;
      }
    }
  }
}
</style>
