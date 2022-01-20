<template>
  <div id="app">
    <Navbar />
    <Header />
    <SectionMeetSEO/>
    <SectionServices/>
    <SectionWork/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Navbar from './components/Navbar.vue';
import SectionMeetSEO from './components/SectionMeetSEO.vue';
import SectionServices from './components/SectionServices.vue';
import SectionWork from './components/SectionWork.vue';

export default {
  name: "App",
  components: {
    Navbar,
    Header,
    SectionMeetSEO,
    SectionServices,
    SectionWork,
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
