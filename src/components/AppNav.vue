<template>
  <div class="nav-container">
    <div class="nav">
      <div class="logo-container">
        <img src="../assets/img/dc-logo.png" alt="DCLogo" />
      </div>
      <ul>
        <li
          v-for="(navItem, index) in nav"
          :key="index"
          :class="index === currentItem ? 'active' : ''"
          @click="thisNav(index)"
        >
          <a href="#">{{ navItem.text }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppNav",
  data: function () {
    return {
      currentItem: 0,
      nav: [
        {
          url: "#",
          text: "Characters",
          active: false,
        },
        {
          url: "#",
          text: "Comics",
          active: false,
        },
        {
          url: "#",
          text: "Movies",
          active: false,
        },
        {
          url: "#",
          text: "TV",
          active: false,
        },
        {
          url: "#",
          text: "Games",
          active: false,
        },
        {
          url: "#",
          text: "Collectibles",
          active: false,
        },
        {
          url: "#",
          text: "Videos",
          active: false,
        },
        {
          url: "#",
          text: "Fans",
          active: false,
        },
        {
          url: "#",
          text: "News",
          active: false,
        },
        {
          url: "#",
          text: "Shop",
          active: false,
        },
      ],
    };
  },
  methods: {
    thisNav(index) {
      this.currentItem = index;
    },
  },
};
</script>

<style lang="scss" scoped>
$blue: #0282f9;
$text-icons-color: #797979;

.nav-container {
  width: 100%;
  height: 80px;
  background-color: white;
  font-size: 0.7rem;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 70%;
  height: 80px;
  margin: 0 auto;
}

.logo-container {
  width: 6%;
}

ul {
  width: 65%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

li {
  line-height: 75px;
  border-bottom: 5px solid transparent;
  &:hover {
    border-bottom: 5px solid $blue;
    a {
      color: $blue;
    }
  }
}

.active {
  border-bottom: 5px solid $blue;
  color: $blue;
}

a {
  color: inherit;
}
</style>
