<template>
<v-col>
  <div >
    <div id="rrss" align="center">
      <ul >
        <li>
          <a >   <img height="150" width="150" :src="Logo" /> </a>
        </li>
      </ul>
    </div>
  </div>
  </v-col>
</template>

<script>
//import { Bubble } from 'vue-burger-menu'
import foto from "@/assets/foto.png";
//import logo from '@/assets/logoAKB.png'
import logo from "@/assets/branding/logoAppBasico.svg";
import wallpaper from "@/assets/branding/App-3.svg";
import behance from "@/assets/rrss/behance-perspective.png";
import gmail from "@/assets/rrss/gmail-google-perspective.png";
import linkedin from "@/assets/rrss/linkedin-perspective.png";
import instagram from "@/assets/rrss/instagram-insta-perspective.png";
import man from "@/assets/recursosVisuales/man.png";
import cv from "@/assets/recursosVisuales/CV.png";
import logo3D from "@/assets/branding/logoApp.svg";

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

h2 {
  font-family: "Roboto";
  color: #ffffff;
  font-style: normal;
  font-weight: normal;
  font-size: 1.2em;
  line-height: 35px;
  text-align: center;
}

#rrss {
  position: relative;
  width: 100%;
  height: 100%;
  
}

ul {
  list-style-type: none;
  margin: 0;
 
  overflow: hidden;
 
}

li {
  float: center;
}

li a {
  display: block;
  color: white;
  text-align: center;
 
  text-decoration: none;
  width: "5%";
}

li a:hover {
  box-shadow: 0 8px 32px 0 rgba(193, 193, 196, 0.37);
  backdrop-filter: blur(5.5px);
  -webkit-backdrop-filter: blur(5.5px);
  border-radius: 100px;
;
}


</style>
