<template>
  <v-flex fluid="true" width="100%">
    <v-img height="500" :src="tablero">
      <v-col>
        <h1 color="#fff">Portafolio</h1>

        <v-row>
          <v-col>
            <div>
              <v-card @click="dialog = true" id="tarjeta-inactiva">
                <v-col>
                  <h3>UI/UX</h3>

                  <v-row align="center">
                    <img id="figma" :src="figma" class="ma-8" />

                    <div class="padre-flex">
                      <div class="content">
                        <div class="padre">
                          <font class="texto_boton" color="#fff"
                            >Prototipos Figmas
                          </font>
                        </div>
                      </div>
                    </div>
                  </v-row>
                </v-col>
              </v-card>
            </div>
          </v-col>
          <!--///////////////////////-->
          <v-col>
            <div>
              <v-card @click="dialog2 = true" id="tarjeta-inactiva">
                <v-col>
                  <h3>Android</h3>

                  <v-row>
                    <img width="20%" :src="android" class="ma-8" />

                    <div class="padre-flex">
                      <div class="content">
                        <div class="padre">
                          <font class="texto_boton" color="#fff"
                            >App PlayStores
                          </font>
                        </div>
                      </div>
                    </div>
                  </v-row>
                </v-col>
              </v-card>
            </div>
          </v-col>
          <!--///////////////////////-->
          <v-col>
            <div>
              <v-card @click="dialog3 = true" id="tarjeta-inactiva">
                <v-col>
                  <h3>Vuejs</h3>

                  <v-row>
                    <img width="25%" :src="vue" class="ma-9" />

                    <div class="padre-flex">
                      <div class="content">
                        <div class="padre">
                          <font class="texto_boton" color="#fff"
                            >App Vuejs
                          </font>
                        </div>
                      </div>
                    </div>
                  </v-row>
                </v-col>
              </v-card>
            </div>
          </v-col>
          <!--///////////////////////-->
        </v-row>
      </v-col>
    </v-img>
    <!--////////Diseño UI/UX///////////////-->

    <template>
      <v-row justify="center">
        <v-dialog
          v-model="dialog"
          fullscreen
          hide-overlay
          transition="dialog-bottom-transition"
        >
          <v-card>
            <v-toolbar dark color="#001">
              <v-btn icon dark @click="dialog = false">
                <v-icon>mdi-close</v-icon>
              </v-btn>
              <v-toolbar-title>Diseño UI/UX</v-toolbar-title>
              <v-spacer></v-spacer>
              <v-toolbar-items>
                <v-btn dark text @click="dialog = false"> Salir </v-btn>
              </v-toolbar-items>
            </v-toolbar>
            <v-carousel v-model="model">
              <v-carousel-item v-for="(color, i) in colors" :key="color">
                <v-sheet :color="color" height="100%" tile>
                  <v-row class="fill-height" align="center" justify="center">
                    <div class="text-h2">Proyecto {{ i + 1 }}</div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>

            <v-divider></v-divider>
            <v-card flat class="d-flex justify-center">
              <v-btn>
                <h3>Enlace</h3>
              </v-btn>
            </v-card>
          </v-card>
        </v-dialog>
      </v-row>
    </template>

    <!--//////////Android/////////////-->
    <template>
      <v-row justify="center">
        <v-dialog
          v-model="dialog2"
          fullscreen
          hide-overlay
          transition="dialog-bottom-transition"
        >
          <v-card>
            <v-toolbar dark color="#a4c639">
              <v-btn icon dark @click="dialog2 = false">
                <v-icon>mdi-close</v-icon>
              </v-btn>
              <v-toolbar-title>Android</v-toolbar-title>
              <v-spacer></v-spacer>
              <v-toolbar-items>
                <v-btn dark text @click="dialog2 = false"> Salir </v-btn>
              </v-toolbar-items>
            </v-toolbar>
            <v-carousel v-model="model_android">
              <v-carousel-item v-for="(color, i) in colors" :key="color">
                <v-sheet :color="color" height="100%" tile>
                  <v-row class="fill-height" align="center" justify="center">
                    <div class="text-h2">Proyecto {{ i + 1 }}</div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>
            <v-divider></v-divider>
            <v-card flat class="d-flex justify-center">
              <v-btn color="#a4c639">
                <h3>Enlace</h3>
              </v-btn>
            </v-card>
          </v-card>
        </v-dialog>
      </v-row>
    </template>

    <!--///////// frontend//////////////-->
    <template>
      <v-row justify="center">
        <v-dialog
          v-model="dialog3"
          fullscreen
          hide-overlay
          transition="dialog-bottom-transition"
        >
          <v-card>
            <v-toolbar dark color="#4b5a">
              <v-btn icon dark @click="dialog3 = false">
                <v-icon>mdi-close</v-icon>
              </v-btn>
              <v-toolbar-title>Vuejs</v-toolbar-title>
              <v-spacer></v-spacer>
              <v-toolbar-items>
                <v-btn dark text @click="dialog3 = false"> Salir </v-btn>
              </v-toolbar-items>
            </v-toolbar>
            <v-carousel v-model="model_vue">
              <v-carousel-item v-for="(color, i) in colors" :key="color">
                <v-sheet height="100%" tile>
                  <v-row class="fill-height" align="center" justify="center">
                    <div class="text-h2">Slide {{ i + 1 }}</div>
                  </v-row>
                </v-sheet>
              </v-carousel-item>
            </v-carousel>

            <v-divider></v-divider>
            <v-card flat class="d-flex justify-center">
              <v-btn color="#4b5a">
                <h3>Enlace</h3>
              </v-btn>
            </v-card>
          </v-card>
        </v-dialog>
      </v-row>
    </template>

    <!--///////////////////////-->
  </v-flex>
</template>

<script>
import foto from "@/assets/foto.png";
import tabla from "@/assets/recursosVisuales/tabla.png";
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
import vue from "@/assets/vue.webp";
import android from "@/assets/android.webp";
import figma from "@/assets/figma.webp";
import d3 from "@/assets/recursosVisuales/3d.png";
import estrellas_movil from "@/assets/estrellometro-movil.svg";
import carpeta from "@/assets/recursosVisuales/carpeta.png";
import estrellas_ux from "@/assets/estrellometro-ux.svg";
import java from "@/assets/java.svg";
import tablero from "@/assets/fondo.webp";

export default {
  name: "App",

  data: () => ({
    model: 0,
    model_android: 0,
    model_vue: 0,
    colors: ["primary", "secondary", "yellow darken-2", "red", "orange"],
    tablero: tablero,
    dialog: false,
    dialog2: false,
    dialog3: false,
    notifications: false,
    sound: true,
    widgets: false,

    java: java,
    vue: vue,
    android: android,
    figma: figma,
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
    portafol: false,
    estrellas_movil: estrellas_movil,
  }),
  methods: {
    Portafolio_fn() {
      this.Vue.prototype.$portafol = true;

      console.log(this.$portafol);
    },
  },

  components: {
    //Carousel3d,
    //Slide,
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
  color: #fff;
  font-style: normal;
  font-weight: normal;
  font-size: 2.1em;
  line-height: 59px;
  text-align: center;
}

h3 {
  font-family: "Roboto";
  color: #000000;
  font-style: normal;
  font-weight: normal;
  font-size: 1.4em;
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
  border-radius: 60px;
}

#tarjeta-inactiva:hover {
  background: rgba(15, 18, 22, 0.8);
  box-shadow: 0 8px 32px 0 rgba(193, 193, 196, 0.37);
  backdrop-filter: blur(5.5px);
  -webkit-backdrop-filter: blur(5.5px);
  border-radius: 35px;
  color: #ffffff;
  .texto_boton {
    color: #ffffff;
  }

  h3 {
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
  box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.5);
  border-radius: 35px;

  .texto_boton {
    color: #000;
  }
}

#figma {
  width: 15%;
}

#android {
  width: 110%;
  height: 50px;
}

#vue {
  width: 110%;
  height: 35px;
}

@media screen and (min-width: 199px) and (max-width: 320px) {
  h1 {
    font-size: 1.6em;
    text-align: center;
    font-family: "Roboto";
  }

  h3 {
    font-size: 1em;
    text-align: center;
    font-family: "Roboto";
  }

  #android {
    width: 500px;
    height: 200px;
  }

  #figma {
    width: 80%;
    height: 50px;
  }

  #vue {
    width: 110%;
    height: 35px;
  }

  #tarjeta-inactiva {
    position: absolute;
    width: 30%;
    height: 300px;
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    background: rgba(255, 255, 255, 0.3);
    box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.5);
    border-radius: 35px;

    .texto_boton {
      color: #000;
      font-size: 0.9em;
      text-align: center;
    }
  }

  #tarjeta-inactiva:hover {
    background: rgba(15, 18, 22, 0.8);
    box-shadow: 0 8px 32px 0 rgba(193, 193, 196, 0.37);
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    border-radius: 35px;
    color: #ffffff;
    .texto_boton {
      color: #ffffff;
    }
  }
}

@media screen and (min-width: 321px) and (max-width: 767px) {
  h1 {
    font-size: 1.6em;

    text-align: center;

    font-family: "Roboto";
  }
  h3 {
    font-size: 1.3em;

    text-align: center;

    font-family: "Roboto";
  }

  #android {
    width: 110%;
    height: 50px;
  }

  #figma {
    width: 80%;
    height: 50px;
  }

  #vue {
    width: 110%;
    height: 35px;
  }

  #tarjeta-inactiva {
    position: absolute;
    width: 30%;
    height: 300px;
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    background: rgba(255, 255, 255, 0.3);
    box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.5);
    border-radius: 35px;

    .texto_boton {
      color: #000;
      font-size: 0.9em;
      text-align: center;
    }
  }

  #tarjeta-inactiva:hover {
    background: rgba(15, 18, 22, 0.8);
    box-shadow: 0 8px 32px 0 rgba(193, 193, 196, 0.37);
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    border-radius: 35px;
    color: #ffffff;
    .texto_boton {
      color: #ffffff;
    }
  }
}

@media screen and (min-width: 768px) and (max-width: 1024px) {
  h1 {
    font-size: 1em;
  }
}
</style>
