<template>

 <div id='rrss'>
    <ul>
      <li>
        <a class="fondo"> <img height="65" width="74" :src="Gmail" /> </a>
      </li>
      <li>
        <a href="#news"> <img height="65" width="74" :src="Behance" /></a>
      </li>
      <li>
        <a href="#contact"> <img height="65" width="74" :src="Linkedin" /> </a>
      </li>
      <li>
        <a href="#about"> <img height="65" width="74" :src="Instagram" /> </a>
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
import behance from "@/assets/rrss/behance-perspective.png";
import gmail from "@/assets/rrss/gmail-google-perspective.png";
import linkedin from "@/assets/rrss/linkedin-perspective.png";
import instagram from "@/assets/rrss/instagram-insta-perspective.png";
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
};
</script>

<style  >
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
backdrop-filter: blur( 5.5px );
-webkit-backdrop-filter: blur( 5.5px );
border-radius: 10px;
  border-radius: 15px;
}
</style>
