<template>
  <div id="app">
    <AppNav />
    <AppContent />
    <AppMenu />
    <AppJumboFooter />
    <AppFooter />
  </div>
</template>

<script>
import AppNav from "./components/AppNav.vue";
import AppContent from "./components/AppContent.vue";
import AppMenu from "./components/AppMenu.vue";
import AppJumboFooter from "./components/AppJumboFooter.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppNav,
    AppContent,
    AppMenu,
    AppJumboFooter,
    AppFooter
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
</style>
