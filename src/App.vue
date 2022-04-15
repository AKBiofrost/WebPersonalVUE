<template>
  <v-app>
    <v-main>
      <body>
        <div id="app">
          <Particles />
        </div>
        <Bubble>
          <a id="home" href="#">
            <span>Home</span>
          </a>

          <a id="test" href="test">
            <span>Test</span>
          </a>

          <div id="nav">
            <router-link to="/">Home</router-link> |
            <router-link to="/about">About</router-link>
          </div>
        </Bubble>
        <router-view />

        <v-col align="center">
          <cabecera></cabecera>

          <v-col justify="center">
            <div class="titulo">
              <h1>Alexander K.Biofröst</h1>
            </div>

            <div class="Subtitulo">
              <h2>Diseñador de Productos</h2>
            </div>
            <redes class="d-flex justify-center"></redes>
          </v-col>

          <tableros></tableros>
        </v-col>
      </body>
    </v-main>
  </v-app>
</template>

<script>
import { Bubble } from "vue-burger-menu";
import cabecera from "@/components/cabecera.vue";
import tableros from "@/components/tableros.vue";
import redes from "@/components/redesSociales.vue";
import fondo from "@/assets/fondo.png";
import Particles from "@/components/particles.vue";

export default {
  name: "App",

  data: () => ({
    redes: redes,
    tableros: tableros,
    cabecera: cabecera,
    Fondo: fondo,
  }),
  components: {
    Bubble, // Register your component,
    cabecera,
    tableros,
    redes,
    Particles,
  },
};
</script>

<style lang="scss" scoped>
.v-card.on-hover.theme--dark {
  background-color: rgba(#fff, 0.8);
}

.padre {
  position: relative;
}
.hijo {
  position: absolute;
  top: 50%;
  left: 50%;
  height: 30%;
  width: 50%;
  margin: -15% 0 0 -25%;
}

.icono {
  width: "5%";
}
.contenedor {
  display: flex;
  justify-content: space-between;
}

h1 {
  font-family: "Roboto";
  color: #ffffff;
  font-style: normal;
  font-weight: normal;
  font-size: 2.1em;
  line-height: 59px;
  text-align: center;
}
.fondo {
  width: 100%;
  height: 100vh;
}
body {
  height: 140%;
  background-image: url("https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgEwb23ce3OWGfCQnerMdrSKNIhBCJ-rkTWJObX2FqUVMfoke_tWdmpRTYw2zpndY3AXhrTq0oG3EREsA6tXOvoSQptTV3DuHDukFurW1qdATu1Pe8LHDl2nN6KnHSO72JKHUZNi_Fgx41v-lu318HmowBXTvBxOpUfdoPHgkId3aYQBwuZUArlUdTJ/s16000/fondo.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
}

h2 {
  font-family: "Roboto";
  color: #ffffff;
  font-style: normal;
  font-weight: normal;
  font-size: 1.2em;
  line-height: 35px;
  text-align: center;
}
</style>
