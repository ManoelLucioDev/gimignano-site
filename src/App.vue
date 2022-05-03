<template>
  <div id="app">
    <Header />

    <router-view />

    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    Header,
    Footer
  },
};
</script>

<style lang="scss">

@import '@/assets/scss/index.scss';
html,
body {
  height: 100vh;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: $background;
  overflow-x: hidden;
  padding-top: 100px;
}

#app {
  font-family: 'Roboto', sans-serif;
}
</style>
