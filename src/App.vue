<template>
  <div id="app">
    <Navbar />
    <Header />
    <SectionMeetSEO/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Navbar from './components/Navbar.vue';
import SectionMeetSEO from './components/SectionMeetSEO.vue';

export default {
  name: "App",
  components: {
    Navbar,
    Header,
    SectionMeetSEO,
  },
};
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/variables.scss';

#app{
  position: relative;
}
</style>
