<template>


  <carousel-3d>
    <slide v-for="(slide, i) in slides" :index="i" :key="i">
      <img
        :data-index="index"
        :class="{
          current: isCurrent,
          onLeft: leftIndex >= 0,
          onRight: rightIndex >= 0,
        }"
        :src="AJA[i]"
      />

      <img />
    </slide>
  </carousel-3d>
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
import d3 from "@/assets/recursosVisuales/3d.png";
import estrellas_movil from "@/assets/estrellometro-movil.svg";
import carpeta from "@/assets/recursosVisuales/carpeta.png";
import estrellas_ux from "@/assets/estrellometro-ux.svg";
import java from "@/assets/java.svg";
import test from "@/assets/test.svg";
import test2 from "@/assets/test2.svg";
import test3 from "@/assets/test3.svg";
import test4 from "@/assets/test4.svg";
import test5 from "@/assets/test5.svg";
import test6 from "@/assets/test6.svg";
import test7 from "@/assets/test7.svg";
import test8 from "@/assets/test8.svg";
import { Carousel3d, Slide } from "vue-carousel-3d";

export default {
  name: "App",

  data: () => ({
    test: test,
    test2: test2,
    test3: test3,
    test4: test4,
    test5: test5,
    test6: test6,
    test7: test7,
    test8: test8,
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
    slides: 7,
    AJA: [test, test2, test3, test4, test5, test6, test7, test8],
    colors: ["primary", "secondary", "yellow darken-2", "red", "orange"],
    //
  }),
  methods: {
    Portafolio_fn() {
      this.Vue.prototype.$portafol = true;
     
      console.log(this.$portafol);
    },
  },
  components: {
    Carousel3d,
    Slide,
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

@media screen and (min-width: 199px) and (max-width: 320px) {
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


}

  .texto_boton {
    font-size: 1em;
  }
  h1 {
    font-size: 1.3em;
  }
  img {
    width: 100%;
    height: 100%;
    align-content: center;
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


}

  .texto_boton {
    font-size: 1em;
  }
  h1 {
    font-size: 1.3em;
  }
  img {
    width: 100%;
    height: 100%;
    align-content: center;
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

    img {
    width: 100%;
    height: 100%;
    align-content: center;
  }
}





</style>
