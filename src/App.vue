<template>
  <v-app>
    <v-navigation-drawer
    v-model="drawer"
    permanent
    theme="dark"
  >
    <v-list-item
      prepend-icon="mdi-account"
      title="Admin"
    ></v-list-item>

    <v-divider></v-divider>

    <v-list density="compact" nav>
      <v-list-item prepend-icon="mdi-view-dashboard" title="Home" value="home" to="/"></v-list-item>
      <v-list-item prepend-icon="mdi-table" title="Manage" value="manage" to="/manage"></v-list-item>
    </v-list>
  </v-navigation-drawer>
  <v-app-bar theme="dark">
    <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    <template v-slot:append>
      <v-btn icon="mdi-heart"></v-btn>

      <v-btn icon="mdi-magnify"></v-btn>

      <v-btn icon="mdi-dots-vertical"></v-btn>
    </template>
  </v-app-bar>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: !null,
  }),
}
</script>
