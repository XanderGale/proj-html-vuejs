<template>
    <header>
        <div class="container">
            <Navbar/>
        </div>
    </header>
</template>

<script>
import Navbar from './Navbar.vue';

export default {
  name: 'Header',
  components: {
      Navbar,
  }
};
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    header{
        background-image: url('../assets/images/1-hero-image.png');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        padding: 20px 0;
        height: 80vh;
    }

</style>