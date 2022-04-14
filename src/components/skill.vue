<template>
    <v-card
    :color=color
    >


<v-img
  width="30%"
  :src="tabla"
>
</v-img>


    </v-card>
</template>


<script>
//import { Bubble } from 'vue-burger-menu' 
import foto from '@/assets/foto.png'
//import logo from '@/assets/logoAKB.png'
import logo from '@/assets/branding/logo.svg'
import wallpaper from '@/assets/branding/App-3.svg'
import behance from '@/assets/rrss/behance-perspective.png'
import gmail from '@/assets/rrss/gmail-google-perspective.png'
import linkedin from '@/assets/rrss/linkedin-perspective.png'
import instagram from '@/assets/rrss/instagram-insta-perspective.png'
import man from '@/assets/recursosVisuales/man.png'
import cv from '@/assets/recursosVisuales/CV.png'
import logo3D from '@/assets/3dlogo.png'
import cell from '@/assets/recursosVisuales/cell.png'
import tabla from '@/assets/recursosVisuales/tabla.png'
import portafolio from '@/assets/recursosVisuales/portafolio.png'
import d3 from '@/assets/recursosVisuales/3d.png'


export default {
  name: 'App',

  data: () => ({
      tabla:tabla,
    show: true,
    Foto:foto,
    Logo:logo, 
    Wallpaper:wallpaper,
    Behance:behance,
    Gmail:gmail,
    Linkedin:linkedin,
    Instagram:instagram,
    Man:man,
    CV:cv,
    logo3D:logo3D,
    cell:cell,
    portafolio:portafolio,
   d3:d3

    //
  }),
components: {
       // Bubble // Register your component
    }

};
</script>



<style lang="scss" scoped    >


.texto_boton{

  font-size: 1.2em;
}
.v-card.on-hover.theme--dark{

 background-color: rgba(#FFF, 0.8)

}
 


.padre-flex{
       display: flex;
        align-items: center;
}
 
.padre-flex > div{
  margin: 0 auto; /* requerido para alineación horizontal */ 
}






.icono{
width:"5%" 

}

 

h1{

font-family:'Roboto';
color: #FFFFFF;
font-style: normal;
font-weight: normal;
font-size: 2.1em;
line-height: 59px;
text-align: center;

}


h2{

font-family:'Roboto';
color: #FFFFFF;
font-style: normal;
font-weight: normal;
font-size: 1.2em;
line-height: 35px;
text-align: center;

}


</style>
