<template>
  <v-app>
    <v-main>
      <div class="fondo" v-if="BoolWelcome == false">
        <v-img class="padre" height="100%" :src="Fondo">
          <Particles />
          <div class="hijo" aling="center">
            <v-row justify="center">
              <breeding-rhombus-spinner
                :animation-duration="2000"
                :size="120"
                :color="'#fff'"
              />
            </v-row>
            <h1>Bienvenido</h1>
          </div>
        </v-img>
      </div>

      <div v-if="BoolWelcome">
        <div class="fondo">
          <v-img class="padre" height="100%" :src="Fondo">
            <body>
              <div id="app">
                <Particles />
              </div>

              <v-col align="center">
                <cabecera class="d-flex justify-center"></cabecera>
                
               
                  <div class="titulo">
                    <h1 v-if="BoolWelcome">Alexander K.Biofröst</h1>
                  </div>

                 

                  <div class="Subtitulo">
                    <h2>Diseñador de Productos</h2>
                  </div>
                  <v-col justify="center">
                    <redes class="d-flex justify-center"></redes>
                  </v-col>

                  <tableros></tableros>
            
              </v-col>
            </body>
          </v-img>
        </div>
      </div>
    </v-main>
  </v-app>
</template>

<script>
//import { Bubble } from "vue-burger-menu";
import cabecera from "@/components/cabecera.vue";
import tableros from "@/components/tableros.vue";
import redes from "@/components/redesSociales.vue";
import fondo from "@/assets/fondo.png";
import Particles from "@/components/particles.vue";
//import { AtomSpinner } from "epic-spinners";
//import { HollowDotsSpinner } from "epic-spinners";
//import { PixelSpinner } from "epic-spinners";
//import { IntersectingCirclesSpinner } from "epic-spinners";
//import { ScalingSquaresSpinner } from "epic-spinners";
//import { HalfCircleSpinner } from "epic-spinners";
//import { TrinityRingsSpinner } from "epic-spinners";
//import { FulfillingSquareSpinner } from "epic-spinners";
//import { CirclesToRhombusesSpinner } from "epic-spinners";
//import { SemipolarSpinner } from "epic-spinners";
//import { FulfillingBouncingCircleSpinner } from "epic-spinners";
import { BreedingRhombusSpinner } from "epic-spinners";

export default {
  name: "App",

  data: () => ({
    redes: redes,
    tableros: tableros,
    cabecera: cabecera,
    Fondo: fondo,
    BoolWelcome: false,
    show: true,
  }),
  mounted: function () {
    setTimeout(() => {
      this.BoolWelcome = true;
      console.log("contador de tiempo" + this.BoolWelcome);
    }, 8000),
      this.$nextTick(function () {});
  },

  components: {
    // Bubble, // Register your component,
    cabecera,
    tableros,
    redes,
    Particles,

    BreedingRhombusSpinner,
  },
};
</script>

<style lang="scss" scoped>
.slide-fade-enter-active {
  transition: all 0.3s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.v-card.on-hover.theme--dark {
  background-color: rgba(#fff, 0.8);
}

.padre {
  position: relative;
}
.hijo {
  position: absolute;
  top: 70%;
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
#body {
  height: 120%;
  background-image: url("https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgEwb23ce3OWGfCQnerMdrSKNIhBCJ-rkTWJObX2FqUVMfoke_tWdmpRTYw2zpndY3AXhrTq0oG3EREsA6tXOvoSQptTV3DuHDukFurW1qdATu1Pe8LHDl2nN6KnHSO72JKHUZNi_Fgx41v-lu318HmowBXTvBxOpUfdoPHgkId3aYQBwuZUArlUdTJ/s16000/fondo.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  position: absolute;
}
#fondo {
  height: 120%;
  background-image: url("https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgEwb23ce3OWGfCQnerMdrSKNIhBCJ-rkTWJObX2FqUVMfoke_tWdmpRTYw2zpndY3AXhrTq0oG3EREsA6tXOvoSQptTV3DuHDukFurW1qdATu1Pe8LHDl2nN6KnHSO72JKHUZNi_Fgx41v-lu318HmowBXTvBxOpUfdoPHgkId3aYQBwuZUArlUdTJ/s16000/fondo.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  position: absolute;
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
