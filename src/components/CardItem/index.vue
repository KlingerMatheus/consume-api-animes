<template>
  <v-lazy>
    <div class="d-flex card-container">
      <v-card
        ripple
        tile
        class="my-5 mx-auto card-style"
        v-for="item in animes"
        :key="item.anime_id"
        color="blue"
      >
        <v-img
          height="300px"
          :src="item.anime_img"
          class="align-center"
        ></v-img>
        <v-card-title>
          <div class="text-capitalize test text-center">
            {{ titleTreatment(item.anime_name) }}
          </div></v-card-title
        >
      </v-card>
    </div></v-lazy
  >
</template>

<script>
import "./style.css";

export default {
  name: "CardItem",
  props: ["animes"],
  methods: {
    titleTreatment(string) {
      return string.replaceAll("_", " ");
    },
  },
};
</script>
