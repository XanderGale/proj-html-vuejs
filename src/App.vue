<template>
  <div id="app">
    <Navbar />
    <Header />
    <SectionMeetSEO/>
    <SectionServices/>
    <SectionWork/>
    <SectionPlans/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Navbar from './components/Navbar.vue';
import SectionMeetSEO from './components/SectionMeetSEO.vue';
import SectionServices from './components/SectionServices.vue';
import SectionWork from './components/SectionWork.vue';
import SectionPlans from './components/SectionPlans.vue';

export default {
  name: "App",
  components: {
    Navbar,
    Header,
    SectionMeetSEO,
    SectionServices,
    SectionWork,
    SectionPlans,
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
