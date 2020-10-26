/* eslint-disable vue/attribute-hyphenation */
<template>
  <div class="container">
    <div class="content">
      <div class="left">
        <img src="@/assets/images/memriselogo.svg" alt="" />
      </div>
      <div class="right">
        <ul>
          <li>
            <nuxt-link to="/homes">
              <p class="link-text">Home</p>
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/courses/">
              <p class="link-text">Course</p>
            </nuxt-link>
          </li>
          <li>
            <nuxt-link to="/group">
              <p class="link-text">Group</p>
            </nuxt-link>
          </li>
          <li>
            <button>Subcribe</button>
          </li>
          <li>
            <a-dropdown-button @click="handleButtonClick">
              Languages
              <a-menu slot="overlay" @click="handleMenuClick">
                <a-menu-item key="1">
                  <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
                </a-menu-item>
                <a-menu-item key="2">
                  <nuxt-link :to="switchLocalePath('vi')">Tiếng việt</nuxt-link>
                </a-menu-item>
              </a-menu>
            </a-dropdown-button>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/scss/main.scss";
.nuxt-link-exact-active {
  p {
    border-bottom: 5px #ffc000 solid;
  }
}
.link-text {
  color: white;
  text-shadow: 0px 1px 3px rgba(0, 0, 0, 0.2);
  font-size: 16px;
}
.container {
  width: 100%;
  background-color: #2b3648;
  position: fixed;
  z-index: 100;
  // top: -63px;
  left: 0;
}

.content {
  display: flex;
  justify-content: space-between;
  width: 50%;
  margin: 0 auto;
  background-color: #2b3648;
  padding: 12px 0px;
}

.right {
  width: 60%;
  display: flex;
  align-items: center;
}
.right ul {
  width: 100%;
  display: flex;
  justify-content: space-between;
  list-style-type: none;
}

.right ul li {
  display: flex;
  align-items: center;
}

.right ul li button {
  color: #2b3648;
  background-color: #ffc000;
  font-weight: bold;
  padding: 7px 20px;
  border-radius: 10px;
  font-size: 16px;
  border: none;
  cursor: pointer;
}

.nuxt-link-exact-active {
  color: green;
}
.dropdown {
  background-color: #2b3648;
  color: white;
}
</style>
<script>
export default {
  methods: {
    handleButtonClick(e) {
      console.log("click left button", e);
    },
    handleMenuClick(e) {
      console.log("click", e);
    },
  },
};
</script>
