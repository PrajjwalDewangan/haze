<template>
  <v-app>
    <navbar v-if="!$route.meta.hideNavbar"></navbar>
    <v-main>
      <router-view />
    </v-main>
    <footer></footer>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    Navbar,
    'footer':Footer
  },
  data: () => ({
    //
  }),
};
</script>
<style>
@import url(@/assets/styles.css);
</style>
