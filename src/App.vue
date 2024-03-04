<script>
import AppNav from './components/AppNav.vue';
import AppFooter from './components/AppFooter.vue';
import AppJumbo from './components/AppJumbo.vue';

export default {

  data() {

  },

  components: {
    AppNav,
    AppFooter,
    AppJumbo
  },

}
</script>


<template>
  <AppNav></AppNav>

  <AppJumbo></AppJumbo>

  <AppFooter></AppFooter>
</template>


<style lang="scss">

@use './styles/general' as *;

</style>
