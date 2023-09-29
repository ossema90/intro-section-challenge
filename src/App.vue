<template>
  <v-app>
    <v-main>
      <nav-bar />
      <main-section></main-section>
    </v-main>
  </v-app>
</template>

<script>
import navBar from './components/navBar.vue'
import mainSection from './components/mainSection.vue'
export default {
  name: 'App',

  components: {
    navBar, mainSection
  },

  data: () => ({
    //
  }),
}
</script>
