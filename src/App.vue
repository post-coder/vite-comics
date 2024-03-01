<script>
import AppNav from './components/AppNav.vue';
import AppFooter from './components/AppFooter.vue';
export default {

  data() {

  },

  components: {
    AppNav,
    AppFooter
  },

}
</script>


<template>
  <AppNav></AppNav>

  <AppFooter></AppFooter>
</template>


<style lang="scss">

@use './styles/general' as *;

</style>
