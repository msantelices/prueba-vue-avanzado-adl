<template>
  <div>
    <v-app-bar app
      color="primary"
      dark>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Cursos AlfaWeb</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn elevation="0" color="primary">
          <v-icon>mdi-logout</v-icon>
          Chao world!!
        </v-btn>
        
      </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute left temporary>
      <v-list nav dense>
        <v-list-item-group
          active-class="blue--text text--darken-4"
        >
          <v-list-item>
            <v-list-item-title color="#ffffff">Inicio</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title><router-link to="/admin">Admin</router-link></v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Acerca de</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
  }),
};
</script>

<style scoped>

</style>