<template>



<div class="ogo pa-4"
    align="center" 
   >
 <v-hover
        v-slot="{ hover }"
        open-delay="100"
      >


<v-img
   width="10%" 
  :src="logo3D"

  v-if="hover"
>
</v-img>



<v-img  v-else
   width="10%" 
  :src="Logo"
>
</v-img>




 </v-hover>
</div>

</template>

<script>
//import { Bubble } from 'vue-burger-menu' 
import foto from '@/assets/foto.png'
//import logo from '@/assets/logoAKB.png'
import logo from '@/assets/branding/logoAppBasico.svg'
import wallpaper from '@/assets/branding/App-3.svg'
import behance from '@/assets/rrss/behance-perspective.png'
import gmail from '@/assets/rrss/gmail-google-perspective.png'
import linkedin from '@/assets/rrss/linkedin-perspective.png'
import instagram from '@/assets/rrss/instagram-insta-perspective.png'
import man from '@/assets/recursosVisuales/man.png'
import cv from '@/assets/recursosVisuales/CV.png'
import logo3D from '@/assets/branding/logoApp.svg'

export default {
  name: 'App',

  data: () => ({

    Foto:foto,
    Logo:logo, 
    Wallpaper:wallpaper,
    Behance:behance,
    Gmail:gmail,
    Linkedin:linkedin,
    Instagram:instagram,
    Man:man,
    CV:cv,
    logo3D:logo3D

    //
  }),
components: {
       // Bubble // Register your component
    }

};
</script>



<style  lang="scss" scoped  >


.v-card.on-hover.theme--dark{

 background-color: rgba(#FFF, 0.8)

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



.icono{
width:"5%" 

}
.contenedor{

  display:flex;
    justify-content: space-between;
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
