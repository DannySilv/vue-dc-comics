<template>
  <div id="app">
    <AppNav />
    <AppContent />
    <AppFooter />
  </div>
</template>

<script>
import AppNav from "./components/AppNav.vue";
import AppContent from "./components/AppContent.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppNav,
    AppContent,
    AppFooter,
  },
};
</script>

<style lang="scss">
@import "./style/style.scss";

#app {
  margin: 10px 0;
}
</style>
