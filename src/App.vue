<template>
  <v-app>
    <Menu />
    <v-main>
      <v-container class="mt-5" dense>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Menu from "./components/Menu/index.vue";

export default {
  name: "App",
  components: {
    Menu,
  },
};
</script>
