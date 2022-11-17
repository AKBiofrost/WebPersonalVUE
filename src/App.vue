<template>
  <v-app>
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

    <div v-if="BoolWelcome == true">
      <div class="fondo">
        <v-img  id="wallpaper" class="padre" height="120%" :src="Fondo">
          <div>
            <Particles />
          </div>

          <v-col align="center">
            <cabecera class="d-flex justify-center"></cabecera>

            <div class="titulo">
              <h1 class="titulo" v-if="BoolWelcome">Alexander K.Biofröst</h1>
            </div>

            <div class="Subtitulo">
              <h2>Desarrollador de Productos</h2>
            </div>
            <v-col justify="center">
              <redes class="d-flex justify-center"></redes>
            </v-col>

            <v-row justify="space-around " class="card pa-2">
              <!--///////////////////////-->
              <v-col Justify="center">
                <h1>Portafolio</h1>
                <div>
                  <v-card
                    @click="$vuetify.goTo($refs.portafolio)"
                    id="tarjeta-inactiva"
                  >
                    <v-col Justify="center">
                      <div class="padre">
                        <div>
                          <img width="30%" :src="portafolio" />
                        </div>
                      </div>

                      <div class="padre-flex">
                        <div class="content">
                          <div class="padre">
                            <font class="texto_boton"> Figma/ Android </font>
                          </div>
                        </div>
                      </div>

                      <!-------------------------------------------------->
                    </v-col>
                  </v-card>
                </div>
              </v-col>
              <!--///////////////////////-->
              <v-col>
                <h1>Perfíl</h1>

                <div>
                  <v-card
                    @click="$vuetify.goTo($refs.perfil)"
                    id="tarjeta-inactiva"
                  >
                    <v-col Justify="center">
                      <div class="padre">
                        <div class="texto_boton">
                          <img width="30%" :src="Man" />
                        </div>
                      </div>

                      <div class="padre-flex">
                        <div class="content">
                          <div class="padre">
                            <font class="texto_boton" color="#fff"
                              >Design Thinking</font
                            >
                          </div>
                        </div>
                      </div>
                    </v-col>
                  </v-card>
                </div>
              </v-col>
              <!--///////////////////////-->
              <v-col>
                <h1>Sobre Mí</h1>

                <div>
                  <v-card
                    @click="$vuetify.goTo($refs.experiencia)"
                    id="tarjeta-inactiva"
                  >
                    <v-col Justify="center">
                      <div class="padre">
                        <div class="texto_boton">
                          <img width="30%" :src="CV" />
                        </div>
                      </div>

                      <div class="padre-flex">
                        <div class="content">
                          <div class="padre">
                            <font class="texto_boton" color="#fff">
                              Experiencia</font
                            >
                          </div>
                        </div>
                      </div>
                    </v-col>
                  </v-card>
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-img>

        <div ref="perfil"><perfil></perfil></div>

        <div ref="portafolio" >
          <tableroportafolio></tableroportafolio>
        </div>

        <v-card  ref="experiencia"   class="pa-2">
          <h1 class="clientes">Empresas Atendidas</h1>
          <Carrusel3D></Carrusel3D>
        </v-card>

<v-fab-transition>
<a href="#" class="fab"> <v-icon>mdi-chevron-up</v-icon>   </a>
</v-fab-transition>
         
      </div>
    </div>
  </v-app>
</template>

<script>
import Vue from "vue";
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
import d3 from "@/assets/recursosVisuales/3d.png";
import estrellas_movil from "@/assets/estrellometro-movil.svg";
import carpeta from "@/assets/recursosVisuales/carpeta.png";
import estrellas_ux from "@/assets/estrellometro-ux.svg";
import java from "@/assets/java.svg";
import cabecera from "@/components/cabecera.vue";
import tableros from "@/components/tableros.vue";
import tableroportafolio from "@/components/tablero_portafolio.vue";
import perfil from "@/components/perfil.vue";
import redes from "@/components/redesSociales.vue";
import fondo from "@/assets/fondo.webp";
import Particles from "@/components/particles.vue";
import vue from "@/assets/vue.webp";
import android from "@/assets/android.webp";
import figma from "@/assets/figma.webp";
import Carrusel3D from "@/components/Carrusel3D.vue";
import { BreedingRhombusSpinner } from "epic-spinners";
Vue.prototype.$portafol = false;
export default {
  name: "App",

  data: () => ({
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
    portafol: false,
    estrellas_movil: estrellas_movil,

    vue: vue,
    android: android,
    figma: figma,
    redes: redes,
    tableros: tableros,
    cabecera: cabecera,
    Fondo: fondo,
    BoolWelcome: false,
    slides: 6,

    perfil: false,
    sobremi: false,
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
    //tableros,
    redes,
    Particles,
    //portafolio,
    Carrusel3D,
    //animacion,
    //hyper,
    tableroportafolio,
    perfil,

    //Carousel3d,
    //Slide,

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
  border-radius: 60px;
  color: #ffffff;
  .texto_boton {
    color: #ffffff;
  }
}
.fab{
  font-size: 16px; /* Cambiar el tamaño de la tipografia */
	text-transform: uppercase; /* Texto en mayusculas */
	font-weight: bold; /* Fuente en negrita o bold */
	color: #ffffff; /* Color del texto */
	border-radius: 100px; /* Borde del boton */
	letter-spacing: 2px; /* Espacio entre letras */
	background-color: #4686e5; /* Color de fondo */
	padding: 30px 30px; /* Relleno del boton */
	position: fixed;
	bottom: 30px;
	right: 30px;
	transition: all 100ms ease 50ms;
	box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
	z-index: 99;

}

.fab:hover {
	background-color: #a5502c; /* Color de fondo al pasar el cursor */
	box-shadow: 0px 15px 20px rgba(0, 0, 0, 0.3);
	transform: translateY(-9px);
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
  border-radius: 60px;
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
.clientes {
  color: rgb(0, 0, 0);
}

@media screen and (min-width: 199px) and (max-width: 320px) {
  
    .fab{

		bottom: 20px;
		right: 20px;
    padding: 20px 20px; /* Relleno del boton */
	position: fixed;
	bottom: 30px;
	right: 30px;
   backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);


  }
  
  
  .titulo {
    font-size: 1.2em;
  }
  .wallpaper{
height: 250%;

  }
  .fondo {
    width: 100%;
    height: 100vh;
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
    font-size: 0.8em;
  }
  h1 {
    font-size: 0.8em;
  }
  img {
    width: 70px;
    height: 70px;
  }

  #tarjeta-inactiva {
    position: absolute;
    width: 30%;
    height: 160px;
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    background: rgba(255, 255, 255, 0.3);
    box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
    border-radius: 40px;

    .texto_boton {
      color: #000;
    }
  }
}

@media screen and (min-width: 321px) and (max-width: 767px) {
  
  .fab{

bottom: 20px;
		right: 20px;
    padding: 20px 20px; /* Relleno del boton */
	position: fixed;
	bottom: 30px;
	right: 30px;
 backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);

  }
  
  
  
  .titulo {
    font-size: 1.5em;
  }
 
  .fondo {
    width: 98%;
    height: 100vh;
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
  }
  img {
    width: 70px;
    height: 70px;
  }

  #tarjeta-inactiva {
    position: absolute;
    width: 30%;
    height: 160px;
    backdrop-filter: blur(5.5px);
    -webkit-backdrop-filter: blur(5.5px);
    background: rgba(255, 255, 255, 0.3);
    box-shadow: 0px 0px 30px rgba(0, 0, 0, 0.5);
    border-radius: 40px;

    .texto_boton {
      color: #000;
    }
  }
}

@media screen and (min-width: 768px) and (max-width: 1024px) {
  h1 {
    font-size: 1em;
  }
}
</style>
