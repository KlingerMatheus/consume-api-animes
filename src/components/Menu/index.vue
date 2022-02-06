<template>
  <v-app-bar dense app color="rgb(20,20,30)" class="navbar-top d-flex">
    <router-link
      class="nav-link"
      v-for="link in navlinks"
      :key="link.title"
      :to="link.path"
    >
      <div class="nav-text">{{ link.title }}</div>
    </router-link>
  </v-app-bar>
</template>

<script>
import "./style.css";

export default {
  name: "Menu",
  data: () => {
    return {
      navlinks: [
        { title: "Home", path: "/" },
        { title: "Lista de Animes", path: "/animes" },
      ],
    };
  },
};
</script>
