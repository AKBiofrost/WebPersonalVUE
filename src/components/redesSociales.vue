<template>
  <div id="rrss">
    <ul>
      <li>
        <a class="Linkedin" @click="visitarLinkedin">
          <img height="65" width="74" :src="Linkedin" />
        </a>
      </li>
      <li>
        <a class="Behance" @click="visitarbehance">
          <img height="65" width="74" :src="Behance"
        /></a>
      </li>
      <li>
        <a class="Instagram" @click="visitarInstagram">
          <img height="65" width="74" :src="Instagram" />
        </a>
      </li>
      <li>
        <a class="Gmail" @click="visitarGithub">
          <img height="65" width="74" :src="Gmail" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
//import { Bubble } from 'vue-burger-menu'
import foto from "@/assets/foto.png";
//import logo from '@/assets/logoAKB.png'
import logo from "@/assets/branding/logo.svg";
import wallpaper from "@/assets/branding/App-3.svg";
import behance from "@/assets/rrss/behance-perspective.webp";
//import gmail from "@/assets/rrss/gmail-google-perspective.png";
import gmail from "@/assets/rrss/github-logo.webp";
import linkedin from "@/assets/rrss/linkedin-perspective.webp";
import instagram from "@/assets/rrss/instagram-insta-perspective.webp";
import man from "@/assets/recursosVisuales/man.png";
import cv from "@/assets/recursosVisuales/CV.png";
import logo3D from "@/assets/3dlogo.png";

export default {
  name: "App",

  data: () => ({
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

    //
  }),
  components: {
    // Bubble // Register your component
  },

  methods: {
    visitarInstagram() {
      var win = window.open("https://www.instagram.com/abiofrost/", "_blank");
      // Cambiar el foco al nuevo tab (punto opcional)
      win.focus();
    },
    visitarLinkedin() {
      var win = window.open(
        "https://www.linkedin.com/in/alexanderkbiofrost/",
        "_blank"
      );
      // Cambiar el foco al nuevo tab (punto opcional)
      win.focus();
    },
    visitarbehance() {
      var win = window.open("https://www.behance.net/Abiofrost", "_blank");
      // Cambiar el foco al nuevo tab (punto opcional)
      win.focus();
    },
    visitarGithub() {
      var win = window.open("https://github.com/AKBiofrost", "_blank");
      // Cambiar el foco al nuevo tab (punto opcional)
      win.focus();
    },
  },
};
</script>

<style>
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

h2 {
  font-family: "Roboto";
  color: #ffffff;
  font-style: normal;
  font-weight: normal;
  font-size: 1.2em;
  line-height: 35px;
  text-align: center;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 10;
  overflow: hidden;
}

#rrss {
  position: relative;
  width: 100%;
  height: 100%;
  padding: 10;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 16px;
  text-decoration: none;
  width: "5%";
}

li a:hover {
  box-shadow: 0 8px 32px 0 rgba(193, 193, 196, 0.37);
  backdrop-filter: blur(5.5px);
  -webkit-backdrop-filter: blur(5.5px);
  border-radius: 25px;
}

@media screen and (min-width: 199px) and (max-width: 320px) {
  #titulo {
    font-size: 1em;
  }

  h1 {
    font-size: 1em;
  }
}

@media screen and (min-width: 321px) and (max-width: 767px) {
  img {
    height: 45px;
    width: 54px;
  }

  li a {
    display: block;
    color: white;
    display: flex;
    justify-content: center;
    padding: 7px;
    text-decoration: none;
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
