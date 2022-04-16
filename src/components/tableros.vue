<template>
  <v-row justify="space-around " class=" card pa-2">
    <v-col Justify="center">
      <h1>Portafolio</h1>

      <v-hover v-slot="{ hover }" open-delay="200">
        <div v-if="hover">
          <v-card
            :elevation="hover ? 16 : 2"
            :class="{ 'on-hover': hover }"
            id="tarjeta"
          >
            <v-col Justify="center">
              <div class="padre">
                <div class="texto_boton">
                  <img width="50%" :src="portafolio" />
                </div>
              </div>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#fff"
                      >Trabajos realizados en las areas de UI/UX, android y
                      3D</font
                    >
                  </div>
                </div>
              </div>

              <!-------------------------------------------------->
            </v-col>
          </v-card>
        </div>

        <div v-else>
          <v-card
            :elevation="hover ? 16 : 8"
            :class="{ 'on-hover': hover }"
            id="tarjeta-inactiva"
          >
            <v-col Justify="center">
              <div class="padre">
                <div class="texto_boton">
                  <img width="50%" :src="portafolio" />
                </div>
              </div>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#000"
                      >Trabajos realizados en las areas de UI/UX, android y
                      3D</font
                    >
                  </div>
                </div>
              </div>

              <!-------------------------------------------------->
            </v-col>
          </v-card>
        </div>
      </v-hover>
    </v-col>

    <v-col>
      <h1>Perfíl</h1>

      <v-hover v-slot="{ hover }" close-delay="200">
        <div v-if="hover">
          <v-card
            :elevation="hover ? 16 : 8"
            :class="{ 'on-hover': hover }"
            id="tarjeta"
          >
            <v-col Justify="center">
              <div class="padre">
                <div class="texto_boton">
                  <img width="50%" :src="Man" />
                </div>
              </div>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#fff"
                      >Diseñador de Productos con 6 años de experiencia</font
                    >
                  </div>
                </div>
              </div>
            </v-col>
          </v-card>
        </div>

        <div v-else>
          <v-card
            :elevation="hover ? 16 : 8"
            :class="{ 'on-hover': hover }"
            id="tarjeta-inactiva"
          >
            <v-col Justify="center">
              <div class="padre">
                <div class="texto_boton">
                  <img width="50%" :src="Man" />
                </div>
              </div>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#000"
                      >Diseñador de Productos con 6 años de experiencia</font
                    >
                  </div>
                </div>
              </div>

              <!-------------------------------------------------->
            </v-col>
          </v-card>
        </div>
      </v-hover>
    </v-col>

    <v-col>
      <h1>Sobre Mí</h1>


<v-hover v-slot="{ hover }" close-delay="200">
        <div v-if="hover">
          <v-card
            :elevation="hover ? 16 : 8"
            :class="{ 'on-hover': hover }"
            id="tarjeta"
          >
            <v-col Justify="center">
              <div class="padre">
                <div class="texto_boton">
                  <img width="50%" :src="CV" />
                </div>
              </div>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#fff"
                      >Me llamo Carlos Delgado, me especializo en diseño de productos digitales</font
                    >
                  </div>
                </div>
              </div>
            </v-col>
          </v-card>
        </div>

        <div v-else>
          <v-card
            :elevation="hover ? 16 : 8"
            :class="{ 'on-hover': hover }"
            id="tarjeta-inactiva"
          >
            <v-col Justify="center">
              <div class="padre">
                <div class="texto_boton">
                  <img width="50%" :src="CV" />
                </div>
              </div>

              <div class="padre-flex">
                <div class="content">
                  <div class="padre">
                    <font class="texto_boton" color="#000"
                      >Me llamo Carlos Delgado, me especializo en diseño de productos digitales</font
                    >
                  </div>
                </div>
              </div>

              <!-------------------------------------------------->
            </v-col>
          </v-card>
        </div>
      </v-hover>
     
    </v-col>
  </v-row>
</template>

<script>
//import { Bubble } from 'vue-burger-menu'
import foto from "@/assets/foto.png";
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
    //java1:java1,
    //java2:java2,
    java: java,
    estrellas_ux: estrellas_ux,
    carpeta: carpeta,
    tabla: tabla,
    show: true,
    Foto: foto,
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
    estrellas_movil: estrellas_movil,
    slides: [
      //java1,
      //java2,
    ],
    //
  }),
  components: {
    // Bubble // Register your component
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
  color: #ffffff;
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

#tarjeta {
  position: absolute;
  width: 30%;
  height: 2.2hv;

  background: rgba(15, 18, 22, 0.8);
  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
  border-radius: 40px;
}



#tarjeta-inactiva {
  position: absolute;
  width: 30%;
  height: 2.2hv;

  background: rgba(255, 255, 255, 0.8);
  box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
  border-radius: 40px;
}
</style>
