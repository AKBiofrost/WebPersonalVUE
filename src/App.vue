<template>
 <v-app>
 <v-main>
<v-card
 color="#1569EF"
 height="100%"
>
 <Bubble     >
      <a id="home" href="#">
        <span>Home</span>
      </a>
    </Bubble>

<v-col  align="center" >

<div class="  logo pa-4"
    align="center" 
   >
 <v-hover
        v-slot="{ hover }"
        open-delay="100"
      >

<dic v-if="hover">
<v-img
   width="10%" 
  :src="logo3D"
>
</v-img>
</dic>

<dic v-else>
<v-img
   width="10%" 
  :src="Logo"
>
</v-img>
</dic>



 </v-hover>
</div>

<v-col justify="center"  >

<div  class="titulo"  >
<h1 > Alexander K.Biofröst   </h1>

</div>

<div  class="Subtitulo"  >
<h2 > Diseñador de Productos  </h2>
</div>

<v-row  class="pa-4" justify="center" >

<v-card flat  width="3%"  color="#1569EF">
<v-img
  :src="Gmail"
>
</v-img>
</v-card>
<v-card flat  width="3%"  color="#1569EF">
<v-img
  :src="Behance"
>
</v-img>
</v-card>
<v-card  flat width="3%"  color="#1569EF">
<v-img
  :src="Linkedin"
>
</v-img>
</v-card>
<v-card  flat width="3%"  color="#1569EF">
<v-img
  :src="Instagram"
>
</v-img>
</v-card>
  
  
 


</v-row>

</v-col>


<v-row  justify="space-around " class="card pa-4">


<v-col>
<h1>Portafolio</h1>

    <v-hover
        v-slot="{ hover }"
        open-delay="200"
      >

<div  v-if="hover"    >
  <v-card
  :elevation="hover ? 16 : 2"
  :class="{ 'on-hover': hover }"
 color="#fff"
  >
  <h1>holaaaaaaaaa</h1>
    </v-card>

</div>
 

<div  v-else  >
  <v-card
  :elevation="hover ? 16 : 2"
  :class="{ 'on-hover': hover }"
 color="#1569EF"
  >
  <h1>holaaaaaaaaa</h1>
    </v-card>

</div>


        </v-hover>
    </v-col>

<v-col>
<h1>Perfíl</h1>
  <v-card
  class="rounded-xl"
  elevation="5"
   color="#fff"  >
<v-img
  width="30%"
  :src="Man"
>
</v-img>
<h4>Diseñador de Productos</h4>


    </v-card>

    
    </v-col>
 




<v-col>
<h1>Sobre Mí</h1>
  <v-card
  elevation="5"
   color="#fff"  >


<v-img
  width="30%"
  :src="CV"
>
</v-img>

  <h4>Me llamo Carlos Delgado, focalizo los resultados de mercado diseñando centrado en el usuario.

Trabajo por SCRUM y Design Thinking


</h4>
    </v-card>
    </v-col>

  </v-row>




</v-col>








</v-card>
</v-main>
  </v-app>
</template>

<script>
import { Bubble } from 'vue-burger-menu' 
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
        Bubble // Register your component
    }

};
</script>



<style>


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
