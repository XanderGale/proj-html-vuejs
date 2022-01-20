<template>
  <div id="app">
    <Navbar :linksArray="links" :activeIndex="activeIndex"/>
    <Header />

    <!-- Sections -->
    <SectionMeetSEO/>
    <SectionServices/>
    <SectionWork/>
    <SectionPlans/>
    <SectionNews/>
    <SectionClients/>
    <SectionContactUs/>

    <!-- Footer -->
    <Footer :linksArray="links" :activeIndex="activeIndex"/>
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
import SectionClients from './components/SectionClients.vue';

// Footer
import Footer from './components/Footer.vue';

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
    SectionClients,
    Footer,
  },
  data: function(){
    return {
      activeIndex: 0,
      links: [
        {
          text: 'home',
          url: '#',
        },
        {
          text: 'who we are',
          url: '#',
        },
        {
          text: 'what we do',
          url: '#',
        },
        {
          text: 'where we work',
          url: '#',
        },
        {
          text: 'careers',
          url: '#',
        },
        {
          text: 'news',
          url: '#',
        },
      ]
    }
  }
};
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/variables.scss';

#app{
  position: relative;
}
</style>
