<template>
  <v-app>
   <navbarComponent></navbarComponent>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import navbarComponent from "./components/NavbarComponente.vue"

export default {
  name: 'App',

  data: () => ({
    //
  }),

  components: {
    navbarComponent
  }
};
</script>
