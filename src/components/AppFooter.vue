<template>
  <div class="footer-container">
    <div class="footer-menu">
      <ul class="menu-container">
        <li v-for="(element, index) in footerMenu" :key="index">
          <div class="icon">
            <img :src="`${element.icon}`" :alt="element.text" />
          </div>
          <a href="">{{ element.text }}</a>
        </li>
      </ul>
    </div>
    <div class="footer-links">
      <div class="link-col">
        <h3>Dc Comics</h3>
        <ul>
          <li><a href="">Characters</a></li>
          <li><a href="">Comics</a></li>
          <li><a href="">Movies</a></li>
          <li><a href="">Tv</a></li>
          <li><a href="">Games</a></li>
          <li><a href="">Videos</a></li>
          <li><a href="">News</a></li>
        </ul>
        <h3>Shop</h3>
        <ul>
          <li><a href="">Shop DC</a></li>
          <li><a href="">Shop DC Collectibles</a></li>
        </ul>
      </div>
      <div class="link-col">
        <h3>DC</h3>
        <ul>
          <li><a href="">Terms Of Use</a></li>
          <li><a href="">Privacy Policy (New)</a></li>
          <li><a href="">Ad CHoices</a></li>
          <li><a href="">Advertising</a></li>
          <li><a href="">Jobs</a></li>
          <li><a href="">Subscriptions</a></li>
          <li><a href="">Talent Workshop</a></li>
          <li><a href="">CPSC Certifications</a></li>
          <li><a href="">Ratings</a></li>
          <li><a href="">Shop Help</a></li>
          <li><a href="">Contact Us</a></li>
        </ul>
      </div>
      <div class="link-col-top">
        <h3>Sites</h3>
        <ul>
          <li><a href="">DC</a></li>
          <li><a href="">MAD Magazine</a></li>
          <li><a href="">DC Kids</a></li>
          <li><a href="">DC Universe</a></li>
          <li><a href="">DC Power Visa</a></li>
        </ul>
      </div>
    </div>
    <div class="img-container">
      <img src="../assets/img/dc-logo-bg.png" alt="" />
    </div>
    <div class="footer-bottom">
      <div class="footer-btm-container">
        <button class="btn">Sign-up now!</button>
        <div class="right-section">
          <h2>Follow us</h2>
          <ul>
            <li v-for="(icon, index) in footerIcons" :key="index">
              <div class="icon-container">
                <img :src="`${icon.img}`" :alt="icon.alt" />
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppFooter",
  data: function () {
    return {
      footerMenu: [
        {
          icon: require("../assets/img/buy-comics-digital-comics.png"),
          text: "Digital Comics",
        },
        {
          icon: require("../assets/img/buy-comics-merchandise.png"),
          text: "DC Merchandise",
        },
        {
          icon: require("../assets/img/buy-comics-subscriptions.png"),
          text: "Subscription",
        },
        {
          icon: require("../assets/img/buy-comics-shop-locator.png"),
          text: "Comic Shop Locator",
        },
        {
          icon: require("../assets/img/buy-dc-power-visa.svg"),
          text: "DC Power Visa",
        },
      ],
      footerIcons: [
        {
          img: require("../assets/img/footer-facebook.png"),
          alt: "Facebook",
        },
        {
          img: require("../assets/img/footer-twitter.png"),
          alt: "Twitter",
        },
        {
          img: require("../assets/img/footer-youtube.png"),
          alt: "Youtube",
        },
        {
          img: require("../assets/img/footer-pinterest.png"),
          alt: "Pinterest",
        },
        {
          img: require("../assets/img/footer-periscope.png"),
          alt: "Periscope",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
$blue: #0282f9;
$text-icons-color: #797979;
$footer-bg: #303030;

.footer-container {
  width: 100%;
  height: calc(100vh - 180px);
  display: flex;
  background-image: url("../assets/img/footer-bg.jpg");
  position: relative; // For BONUS 1 & FOOTER-BTM
}

.img-container {
  height: calc(100vh - 180px);
  width: 400px;
  vertical-align: middle;
  float: right;
  display: flex;
  align-items: center;
  margin-right: 15%;
}

.footer-menu {
  width: 100%;
  height: 100px;
  background-color: $blue;
  position: absolute;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  color: white;
  ul {
    height: 50%;
  }
}

.menu-container {
  width: 70%;
  margin: 0 auto;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  font-size: 0.8rem;
}

.menu-container li {
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 0.7rem;
  a {
    color: inherit;
    margin-left: 0.3rem;
  }
}

.icon {
  img {
    width: 40px;
    height: 40px;
    object-fit: scale-down;
  }
}

.footer-links {
  width: 60%;
  padding: 100px 0 80px 15%;
  display: flex;
  margin-top: 1rem;
}

.link-col {
  margin-right: 2rem;
}

.link-col-top {
  align-self: flex-start;
}

h3 {
  color: white;
  font-size: 1rem;
}

li {
  color: $text-icons-color;
  font-size: 0.6rem;
  a {
    color: inherit;
  }
}

.footer-bottom {
  width: 100%;
  height: 80px;
  background-color: $footer-bg;
  position: absolute;
  bottom: 0;
}

.footer-btm-container {
  width: 70%;
  height: 80px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  ul {
    display: flex;
    align-items: center;
    margin-left: 1rem;
  }
}

.btn {
  color: white;
  background-color: $footer-bg;
  border: 2px solid $blue;
  padding: 0.3rem 1rem;
  font-family: "Koulen", cursive;
}

.right-section {
  display: flex;
  align-items: center;
}

h2 {
  color: $blue;
  font-size: 1.2rem;
}

.icon-container {
  width: 70%;
}
</style>
