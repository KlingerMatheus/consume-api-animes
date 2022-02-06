<template>
  <v-lazy>
    <v-card ripple elevation="5" class="pa-10" color="blue">
      <h1>Olá! Meu nome é <b>Klinger Matheus</b>.</h1>
      <h2>
        Este é apenas um teste baseado em consumir uma
        <a href="https://en.wikipedia.org/wiki/API" target="blank"
          ><b>API</b></a
        >
        que fornece dados de alguns <b>animes</b>
      </h2>
      <v-card class="pa-5 mt-5">
        <article>
          <cite>
            Documentação da API:
            <a
              href="https://github.com/chandan-02/anime-facts-rest-api"
              target="_blank"
              >Clique Aqui</a
            >
          </cite>
          <br />
          <cite>
            A API utilizada retorna esses dados:
            <a
              href="https://anime-facts-rest-api.herokuapp.com/api/v1"
              target="_blank"
            >
              Clique Aqui
            </a>
          </cite>
        </article>
      </v-card>
    </v-card>
  </v-lazy>
</template>

<script>
import "./style.css";

export default {
  name: "Home",
};
</script>
