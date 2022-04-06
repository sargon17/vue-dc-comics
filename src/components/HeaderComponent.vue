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
              <a href="#" class="header__nav-item-link">{{ title }}</a>
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

  &__logo-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100px;
    aspect-ratio: 1;

    & > img {
      width: 80px;
    }
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
      &-link {
        position: relative;
        padding: 0 0 43px 0;
        color: #383838;
        text-decoration: none;
        text-transform: uppercase;
        font-size: 14px;
        font-weight: 600;
        transition: color 0.2s ease-in-out;
        &:hover {
          color: #0282f9;

          &:after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: #0282f9;
            transition: transform 0.2s ease-in-out;
          }
        }
      }
    }
  }
}
</style>
