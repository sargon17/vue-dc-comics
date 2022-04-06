<template>
  <div class="footer-top">
    <div class="footer-content">
      <div class="footer-top__content">
        <div class="footer-top__content__nav-list">
          <h3>DC Comics</h3>
          <ul>
            <li class="footer-top__content__nav-item">
              <a href="#">Home</a>
            </li>
            <li>
              <a href="#">About</a>
            </li>
            <li>
              <a href="#">Contact</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer-top__logo">
        <img src="../assets/dc-logo-bg.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterSection",
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
  &__content__nav-list {
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

  &__logo {
    height: 100%;
    overflow: hidden;
    img {
      margin-top: -20%;
    }
  }
}
</style>
