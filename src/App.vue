<template>
  <div id="app">
    <Navbar />
    <Header />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Navbar from './components/Navbar.vue';

export default {
  name: "App",
  components: {
    Header,
    Navbar,
  },
};
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/variables.scss';
</style>
