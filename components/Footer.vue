<template>
  <div class="container">
    <div class="content">
      <div class="left">
        <div class="logo">
          <img
            class="logo-image"
            src="@/assets/images/memriselogo.svg"
            alt=""
          />
        </div>
        <div class="link">
          <a href=""
            ><img src="@/assets/images/facebook.svg" alt="facebook"
          /></a>
          <a href="">
            <img src="@/assets/images/twitter.svg" alt="twitter" />
          </a>
          <a href="">
            <img src="@/assets/images/youtube.svg" alt="youtube"
          /></a>
          <a href="">
            <img src="@/assets/images/instagram.svg" alt="insta"
          /></a>
        </div>
      </div>
      <div class="right">
        <div class="col">
          <ul>
            <li>About us</li>
            <li>Team</li>
            <li>Job</li>
          </ul>
        </div>
        <div class="col">
          <ul>
            <li>About us</li>
            <li>Team</li>
            <li>Job</li>
          </ul>
        </div>
        <div class="col">
          <ul>
            <li>About us</li>
            <li>Team</li>
            <li>Job</li>
          </ul>
        </div>
        <div class="col">
          <ul>
            <li>About us</li>
          </ul>
        </div>
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
}

.content {
  display: flex;
  justify-content: space-between;
  width: 45%;
  margin: 0 10%;
  background-color: #2b3648;
  padding: 12px 0px;
}

.right {
  width: 60%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: white;
}
.right .col ul {
  width: 100%;
  display: flex;
  flex-direction: column;
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
}

.left {
  width: 30%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.nuxt-link-exact-active {
  color: green;
}

.logo-image {
  width: 6em;
}
.link a {
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 56% 48% 53% 56% / 70% 50% 58% 41%;
  padding: 4px;
  color: #2b3648;
  background-color: #f1a278;
  width: calc(25% - 16px);
  max-width: 28px;
}
.link {
  display: flex;
  width: 100%;
  justify-content: space-between;
  margin-top: 2em;
}
.link img {
  width: 2em;
  height: 2em;
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
