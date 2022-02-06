<template>
  <v-container dense>
    <h1>{{ page.title }}</h1>
    <CardItem :animes="this.animes" />
  </v-container>
</template>

<script>
import CardItem from "../../components/CardItem/index.vue";

export default {
  name: "AnimeList",
  components: {
    CardItem,
  },
  created() {
    this.getAnimes();
  },
  data: () => {
    return {
      page: {
        title: "Lista de Animes",
      },
      animes: Array,
    };
  },
  methods: {
    async getAnimes() {
      return await fetch("https://anime-facts-rest-api.herokuapp.com/api/v1")
        .then((response) => response.json())
        .then((json) => {
          this.animes = json.data;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>
