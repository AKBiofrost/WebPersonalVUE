<template>
  <v-app>
    <v-main>
<div class="fondo" v-if="BoolWelcome == false" >


 <v-img height="120%" :src="Fondo">

   <div id="app">
          <Particles />
        </div>

     

<h1>holaaa</h1>
<v-col align="center">
  <v-row align="center" justify="center" >
   <atom-spinner
             :animation-duration="1000"
             :size="60"
             :color="'#ff1d5e'"
     />
     <hollow-dots-spinner
             :animation-duration="1000"
             :size="60"
             :color="'#ff1d5e'"
     />
     <pixel-spinner
        :animation-duration="2000"
        :pixel-size="70"
        :color="'#ff1d5e'"
/>

<scaling-squares-spinner
        :animation-duration="1250"
        :size="65"
        :color="'#ff1d5e'"
/>
    <intersecting-circles-spinner
        :animation-duration="1200"
        :size="70"
        :color="'#ff1d5e'"
/>

<half-circle-spinner
        :animation-duration="1000"
        :size="60"
        :color="'#ff1d5e'"
/>
<trinity-rings-spinner
        :animation-duration="1500"
        :size="66"
        :color="'#ff1d5e'"
/>

</v-row>
<fulfilling-square-spinner
        :animation-duration="4000"
        :size="50"
        :color="'#ff1d5e'"
/>

<circles-to-rhombuses-spinner
        :animation-duration="1200"
        :circles-num="3"
        :circle-size="15"
        :color="'#ff1d5e'"
/>

<semipolar-spinner
        :animation-duration="2000"
        :size="65"
        :color="'#ff1d5e'"
/>

<fulfilling-bouncing-circle-spinner
        :animation-duration="4000"
        :size="60"
        :color="'#ff1d5e'"
/>

<breeding-rhombus-spinner
        :animation-duration="2000"
        :size="65"
        :color="'#ff1d5e'"
/>
 </v-col>    

    </v-img>
</div>
<div  class="fondo" v-else>
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
          <cabecera class="d-flex justify-center"></cabecera>

          <v-col justify="center">
            <div class="titulo">
              <h1>Alexander K.Biofröst</h1>
            </div>

            <div class="Subtitulo">
              <h2>Diseñador de Productos</h2>
            </div>
            <redes class="d-flex justify-center"></redes>
          </v-col>

          <tableros ></tableros>
        </v-col>
      </body>
</div>

     
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
import {AtomSpinner} from 'epic-spinners'
import {HollowDotsSpinner} from 'epic-spinners'
import {PixelSpinner} from 'epic-spinners'
import {IntersectingCirclesSpinner} from 'epic-spinners'
import {ScalingSquaresSpinner} from 'epic-spinners'
import {HalfCircleSpinner} from 'epic-spinners'
import {TrinityRingsSpinner} from 'epic-spinners'
import {FulfillingSquareSpinner} from 'epic-spinners'
import {CirclesToRhombusesSpinner} from 'epic-spinners'
import {SemipolarSpinner} from 'epic-spinners'
import {FulfillingBouncingCircleSpinner} from 'epic-spinners'
import {BreedingRhombusSpinner} from 'epic-spinners'



export default {
  name: "App",

  data: () => ({
    redes: redes,
    tableros: tableros,
    cabecera: cabecera,
    Fondo: fondo,
    BoolWelcome:false,
  }),
 mounted: function () {
    setTimeout(() => {
      this.BoolWelcome = true;
      console.log( "contador de tiempo"+this.BoolWelcome);
    }, 8000),
      this.$nextTick(function () {
        // Código que se ejecutará solo después de
        // haber renderizado la vista completa
        //this.CapturaContrato();
        //this.tamañoPantalla();
       // this.cargardata();
        //this.cargarAlerta();
       // this.GraficoPorPais();
        //this.TimeWelcom()
      });
  },





  components: {
    Bubble, // Register your component,
    cabecera,
    tableros,
    redes,
    Particles,
    AtomSpinner,
    HollowDotsSpinner,
    PixelSpinner,
    IntersectingCirclesSpinner,
    ScalingSquaresSpinner,
    HalfCircleSpinner,
    TrinityRingsSpinner,
    FulfillingSquareSpinner,
    CirclesToRhombusesSpinner,
    SemipolarSpinner,
    FulfillingBouncingCircleSpinner,
    BreedingRhombusSpinner,
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
#fondo{
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
