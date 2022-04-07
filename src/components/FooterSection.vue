<template>
  <div>
    <div class="footer-top">
      <div class="footer-content">
        <div class="footer-top__content">
          <div
            class="footer-top__content__nav-list"
            v-for="{ title, links } in footerNavigationData"
            :key="title"
          >
            <h3>{{ title }}</h3>
            <ul>
              <li
                class="footer-top__content__nav-item"
                v-for="{ title, url } in links"
                :key="title"
              >
                <a :href="url">{{ title }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="footer-top__logo">
          <img src="../assets/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="footer-content">
        <div class="footer-bottom__content">
          <div class="footer-bottom__content__signup">
            <button>Sign-up now!</button>
          </div>
          <div class="footer-bottom__content__social-media">
            <h3>Follow us</h3>
            <ul>
              <li
                class="footer-bottom__content__social-media__item"
                v-for="{ name, url, icon, id } in socialMediaData"
                :key="id"
              >
                <a :href="url">
                  <img :src="icon" :alt="name" />
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import footerNavigationData from "../data/footerNavigationData.json";
import socialMediaData from "../data/socialMediaData.js";

export default {
  name: "FooterSection",
  data() {
    return {
      footerNavigationData,
      socialMediaData,
    };
  },
};
</script>

<style lang="scss" scoped>
.footer-top {
  width: 100%;
  height: 40vh;
  background: #000 url(../assets/footer-bg.jpg) no-repeat center center;
  background-size: cover;
  .footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
  }
  &__content {
    display: flex;
    flex-direction: column;
    max-height: 100%;
    height: 40vh;
    flex-wrap: wrap;
    width: 50vw;
    gap: 20px;
    align-content: start;

    &__nav-list {
      h3 {
        color: #fff;
        font-size: 1rem;
        font-weight: bold;
        text-transform: uppercase;
      }
      ul {
        list-style: none;
        padding: 0;
        li {
          a {
            text-decoration: none;
            color: rgb(137, 137, 137);
            font-size: 0.9rem;
            transition: all 0.3s ease;

            &:hover {
              color: #fff;
            }
          }
        }
      }
    }
  }

  &__logo {
    height: 40vh;
    width: 30vw;
    overflow: hidden;
    img {
      margin-top: -10%;
      width: 100%;
    }
  }
}
.footer-bottom {
  background: #303030;
  .footer-content {
    max-width: 1200px;
    margin: 0 auto;
  }
  &__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 20px;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    &__signup {
      button {
        background: transparent;
        color: #fff;
        border: 2px solid #0282f9;
        padding: 10px 20px;
        font-size: 0.9rem;
        font-weight: 600;
        text-transform: uppercase;
        transition: all 0.3s ease;
        cursor: pointer;
        &:hover {
          background: #fff;
          color: #0282f9;
        }
      }
    }
    &__social-media {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      h3 {
        color: #0282f9;
        font-size: 1rem;
        font-weight: bold;
        text-transform: uppercase;
      }
      ul {
        display: flex;
        justify-content: center;
        align-items: center;
        list-style: none;
        gap: 10px;
        padding: 0;
        li {
          a {
            text-decoration: none;
            color: rgb(137, 137, 137);
            font-size: 0.9rem;
            transition: all 0.3s ease;

            &:hover {
              color: #fff;
            }
          }
        }
      }
    }
  }
}
</style>
