<template>
  <div id="app">
    <Navbar />
    <Header />

    <!-- Sections -->
    <SectionMeetSEO/>
    <SectionServices/>
    <SectionWork/>
    <SectionPlans/>
    <SectionNews/>
    <SectionContactUs/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Header from "./components/Header.vue";
// Sections
import SectionMeetSEO from './components/SectionMeetSEO.vue';
import SectionServices from './components/SectionServices.vue';
import SectionWork from './components/SectionWork.vue';
import SectionPlans from './components/SectionPlans.vue';
import SectionNews from './components/SectionNews.vue';
import SectionContactUs from './components/SectionContactUs.vue';

export default {
  name: "App",
  components: {
    Navbar,
    Header,
    SectionMeetSEO,
    SectionServices,
    SectionWork,
    SectionPlans,
    SectionNews,
    SectionContactUs,
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
