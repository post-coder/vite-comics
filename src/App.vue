<script>
import AppNav from './components/AppNav.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbo from './components/AppJumbo.vue';
import AppComics from './components/AppComics.vue';

export default {

  data() {

  },

  components: {
    AppNav,
    AppFooter,
    AppJumbo,
    AppComics
  },

}
</script>


<template>
  <AppNav></AppNav>

  <AppJumbo></AppJumbo>

  <AppComics></AppComics>
  

  <AppFooter></AppFooter>
</template>


<style lang="scss">

@use './styles/general' as *;

</style>
