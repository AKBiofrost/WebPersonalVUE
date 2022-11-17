<template>
  <v-card height="500" Justify="center" flat class="pa-1">
    <h1 class="clientes"   >Perfíl</h1>
    <v-row justify="space-around " class="card pa-1">
      <!-------------------------------------------------->
      <v-col align="center">
        <div>
          <v-card @click="Portafolio_fn" id="tarjeta-inactiva2">
            <v-col align="center">
              <div class="padre">
                <v-card flat class="foto rounded-xl">
                  <img id="foto" :src="fotos" />
                </v-card>
              </div>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton"> Developer mobile </font>
                  </div>
                </div>
              </div>

              <!-------------------------------------------------->
            </v-col>
          </v-card>
        </div>
      </v-col>
      <!-------------------------------------------------->

      <v-col align="center">
        <h3>Desarrollador de productos</h3>
        <h4>
          Trabajo con las siguientes tecnologias a nivel medio-alto por SCRUM y Design thinking
        </h4>

        <div>
          <v-col Justify="center">
            <v-row justify="space-around">
              <v-card class="ma-3" flat width="20%">
                <img id="android" :src="android" />
              </v-card>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#000"> Nativo </font>
                  </div>
                </div>
              </div>
            </v-row>

            <v-row justify="space-around">
              <v-card class="ma-3" flat width="20%">
                <img id="figma" :src="figma" />
              </v-card>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#000"> Figma</font>
                  </div>
                </div>
              </div>
            </v-row>
            <v-row justify="space-around">
              <v-card class="ma-3" flat width="20%">
                <img id="vue" :src="vue" />
              </v-card>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#000"> Vuejs </font>
                  </div>
                </div>
              </div>
            </v-row>
          </v-col>
        </div>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
//import { Bubble } from 'vue-burger-menu'
//import Vue from "vue";
import foto from "@/assets/foto.png";
import fotos from "@/assets/1.jpg";
import vue from "@/assets/vue.webp";
import android from "@/assets/android.webp";
import figma from "@/assets/figma.webp";
import tabla from "@/assets/recursosVisuales/tabla.png";
//import skill from '@/components/skill.vue'
//import logo from '@/assets/logoAKB.png'
import logo from "@/assets/branding/logo.svg";
import wallpaper from "@/assets/branding/App-3.svg";
import behance from "@/assets/rrss/behance-perspective.png";
import gmail from "@/assets/rrss/gmail-google-perspective.png";
import linkedin from "@/assets/rrss/linkedin-perspective.png";
import instagram from "@/assets/rrss/instagram-insta-perspective.png";
import man from "@/assets/recursosVisuales/man.png";
import cv from "@/assets/recursosVisuales/CV.png";
import logo3D from "@/assets/3dlogo.png";
import cell from "@/assets/recursosVisuales/cell.png";
import portafolio from "@/assets/recursosVisuales/portafolio.png";
import d3 from "@/assets/recursosVisuales/3d.png";
import estrellas_movil from "@/assets/estrellometro-movil.svg";
import carpeta from "@/assets/recursosVisuales/carpeta.png";
import estrellas_ux from "@/assets/estrellometro-ux.svg";
import java from "@/assets/java.svg";
//import java1 from "@/assets/grupo14.svg";
//import java2 from "@/assets/grupo15.svg";

export default {
  name: "App",

  data: () => ({
    vue: vue,
    android: android,
    figma: figma,
    java: java,
    estrellas_ux: estrellas_ux,
    carpeta: carpeta,
    tabla: tabla,
    show: true,
    Foto: foto,
    fotos: fotos,
    Logo: logo,
    Wallpaper: wallpaper,
    Behance: behance,
    Gmail: gmail,
    Linkedin: linkedin,
    Instagram: instagram,
    Man: man,
    CV: cv,
    logo3D: logo3D,
    cell: cell,
    portafolio: portafolio,
    d3: d3,
    portafol: false,
    estrellas_movil: estrellas_movil,
    slides: [
      //java1,
      //java2,
    ],
    //
  }),
  methods: {
    Portafolio_fn() {
      this.Vue.prototype.$portafol = true;
      //console.log("ACCESO A FOTO Y NOMBRE DEL USUARIO");
      console.log(this.$portafol);
    },
  },
};
</script>

<style lang="scss" scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.2s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

/* Las animaciones de entrada y salida pueden usar */
/* funciones de espera y duración diferentes.      */
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

.bounce-enter-active {
  animation: bounce-in 0.5s;
}
.bounce-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}

.texto_boton {
  font-size: 1.2em;
}
.v-card.on-hover.theme--dark {
  background-color: rgba(#fff, 0.8);
}

.hijo {
  line-height: 100px; //Damos 200px de alto para notar el efecto
}
.hijo_estrellometro {
  line-height: 50px; //Damos 200px de alto para notar el efecto
}

.tecnologias {
  margin: auto;
  width: 50%;
  border: 3px solid green;
  padding: 10px;
}

.padre-flex {
  display: flex;
  align-items: center;
}

.padre-flex > div {
  margin: 0 auto; /* requerido para alineación horizontal */
}

.icono {
  width: "5%";
}

h1 {
  font-family: "Roboto";
  color: #000000;
  font-style: normal;
  font-weight: normal;
  font-size: 2.1em;
  line-height: 59px;
  text-align: center;
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

h3 {
  font-family: "Roboto";
  color: #000000;
  font-size: 2.1em;
}

#tarjeta {
  position: absolute;
  width: 30%;
  height: 2.2hv;

  background: rgba(15, 18, 22, 0.8);
  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
  border-radius: 60px;
}

#android {
  width: 60%;
}

#figma {
  width: 50%;
}
#vue {
  width: 60%;
}

#foto {
  width: 100%;
}
.foto {
  width: 60%;
}

#tarjeta-inactiva:hover {
  background: rgba(15, 18, 22, 0.8);
  box-shadow: 0 8px 32px 0 rgba(193, 193, 196, 0.37);
  backdrop-filter: blur(5.5px);
  -webkit-backdrop-filter: blur(5.5px);
  border-radius: 60px;
  color: #ffffff;
  .texto_boton {
    color: #ffffff;
  }
}

#tarjeta-inactiva {
  position: absolute;
  width: 30%;
  height: 2.2hv;
  backdrop-filter: blur(5.5px);
  -webkit-backdrop-filter: blur(5.5px);
  background: rgba(255, 255, 255, 0.3);
  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
  border-radius: 60px;

  .texto_boton {
    color: #000;
  }
}

#tarjeta-inactiva2 {
  position: absolute;
  width: 30%;
  height: 2.2hv;
  backdrop-filter: blur(5.5px);
  -webkit-backdrop-filter: blur(5.5px);
  background: rgba(255, 255, 255, 0.3);
  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
  border-radius: 60px;

  .texto_boton {
    color: #000;
  }
}

@media screen and (min-width: 199px) and (max-width: 320px) {
h3 {
    font-family: "Roboto";
    color: #000000;
    font-size: 1.3em;
  }
  .clientes {
  color: rgb(0, 0, 0);
    font-weight: bold;
    font-size: 1.4em;
    text-align: center;

    font-family: "Roboto";

    line-height: 59px;


}

  .texto_boton {
    font-size: 1em;
  }
  h1 {
    font-size: 1.3em;
       font-weight: bold;
        text-align: center;

    font-family: "Roboto";
  }

  h4 {
    font-size: 0.8em;
  }

  #foto {
    width: 100%;
    height: 100px;
  }
  .foto {
    width: 100%;
  }

  #android {
    width: 100%;
    height: 40px;
  }

  #figma {
    width: 80%;
    height: 40px;
  }

  #vue {
    width: 100%;
    height: 30px;
  }

  #tarjeta-inactiva2 {
    position: absolute;
    width: 40%;
    height: 2.2hv;
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    background: rgba(255, 255, 255, 0.3);
    box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
    border-radius: 30px;

    .texto_boton {
      color: #000;
    }
  }
  #foto {
    width: 60%;
  }
}

@media screen and (min-width: 321px) and (max-width: 767px) {
  h3 {
    font-family: "Roboto";
    color: #000000;
    font-size: 1.3em;
  }
  .clientes {
   color: rgb(0, 0, 0);
    font-weight: bold;
    font-size: 1.5em;
    text-align: center;

    font-family: "Roboto";

    line-height: 59px;


}

  .texto_boton {
    font-size: 1em;
  }
  h1 {
    font-size: 1.3em;
       font-weight: bold;
        text-align: center;

    font-family: "Roboto";
  }

  h4 {
    font-size: 0.8em;
  }

  #foto {
    width: 100%;
    height: 100px;
  }
  .foto {
    width: 100%;
  }

  #android {
    width: 100%;
    height: 50px;
  }

  #figma {
    width: 80%;
    height: 50px;
  }

  #vue {
    width: 100%;
    height: 35px;
  }

  #tarjeta-inactiva2 {
    position: absolute;
    width: 40%;
    height: 2.2hv;
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    background: rgba(255, 255, 255, 0.3);
    box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
    border-radius: 30px;

    .texto_boton {
      color: #000;
    }
  }
  #foto {
    width: 60%;
  }
}

@media screen and (min-width: 640px) and (max-width: 760px) {
  h1 {
    font-size: 1em;
  }
}

@media screen and (min-width: 768px) and (max-width: 1024px) {
  h1 {
    font-size: 1em;
  }
}
</style>
