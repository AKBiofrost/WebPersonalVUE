<template>

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
 class="rounded-xl"
  >




<v-col Justify="center">




  <v-card 
  class="pa-2"
  color="#fff" 
  flat  >


<v-row >

<div>  
<v-img
  width="140"
  :src="cell"
>
</v-img>
</div>

<div class="padre-flex">
	<div class="content">
	


<div    >
<v-card
 height="100%"
  class="rounded-xl pa-3"
   min-width="178"
  elevation="8"
  color="#1569EF"
   :class="{ 'on-hover': hover }"
>
<div class="padre">
<font class="texto_boton" color="#fff">Desarrollo Movil</font>
</div>
</v-card>
</div>


	</div>
</div>
</v-row>
   
  </v-card>





  <v-card 
  class="pa-2"
  color="#fff" 
  flat  >


<v-row >

<div>  
<v-img
  width="140"
  :src="portafolio"
>
</v-img>
</div>

<div class="padre-flex">
	<div class="content">
	


<v-card
 height="100%"
 min-width="178"
  class="rounded-xl pa-3"
  elevation="8"
   color="#1569EF"
   :class="{ 'on-hover': hover }"
  
>
<div class="padre">
<font class="texto_boton"  color="#fff"  >Diseño UI/UX</font>
</div>
</v-card>

	</div>
</div>

</v-row>
   
  </v-card>







  <v-card 
  class="pa-2"
  color="#fff" 
  flat  >


<v-row >

<div>  
<v-img
  width="140"
  :src="d3"
>
</v-img>
</div>

<div class="padre-flex">
	<div class="content">
	


<v-card
 height="100%"
 min-width="178"
  class="rounded-xl pa-3"
  elevation="8"
   color="#1569EF"
   :class="{ 'on-hover': hover }"
>
<div class="padre">
<font class="texto_boton"  color="#fff"    >Diseño 3D</font>
</div>
</v-card>

	</div>
</div>

</v-row>
   
  </v-card>






</v-col>








    </v-card>
</div>
 

<div  v-else  >
  <v-card
  :elevation="hover ? 16 : 2"
  :class="{ 'on-hover': hover }"
 color="#1569EF"
 class="rounded-xl"
  >




  
<v-col Justify="center">

  <v-card 
  class="pa-2"
  color="#1569EF" 
  flat  >


<v-row >

<div>  
<v-img
  width="140"
  :src="cell"
>
</v-img>
</div>

<div class="padre-flex">
	<div class="content">
	

<v-card
 height="100%"
  class="rounded-xl pa-3"
   min-width="178"
  elevation="8"
>
<div class="padre">
<font class="texto_boton">Desarrollo Movil</font>
</div>
</v-card>

	</div>
</div>
</v-row>
   
  </v-card>





  <v-card 
  class="pa-2"
  color="#1569EF" 
  flat  >


<v-row >

<div>  
<v-img
  width="140"
  :src="portafolio"
>
</v-img>
</div>

<div class="padre-flex">
	<div class="content">
	


<v-card
 height="100%"
 min-width="178"
  class="rounded-xl pa-3"
  elevation="8"
>
<div class="padre">
<font class="texto_boton">Diseño UI/UX</font>
</div>
</v-card>

	</div>
</div>

</v-row>
   
  </v-card>







  <v-card 
  class="pa-2"
  color="#1569EF" 
  flat  >


<v-row >

<div>  
<v-img
  width="140"
  :src="d3"
>
</v-img>
</div>

<div class="padre-flex">
	<div class="content">
	


<v-card
 height="100%"
 min-width="178"
  class="rounded-xl pa-3"
  elevation="8"
>
<div class="padre">
<font class="texto_boton">Diseño 3D</font>
</div>
</v-card>

	</div>
</div>

</v-row>
   
  </v-card>






</v-col>



  
  
  
  
    </v-card>

</div>


        </v-hover>
    </v-col>

<v-col>
<h1>Perfíl</h1>

<v-hover
        v-slot="{ hover }"
        open-delay="200"
      >


<div  v-if="hover"    >
  <v-card
  :elevation="hover ? 16 : 8"
  :class="{ 'on-hover': hover }"
  class="rounded-xl"
  
   color="#fff"  >
<v-img
  width="30%"
  :src="Man"
>
</v-img>
<font color="#000">Diseñador de Productos</font>


    </v-card>
</div>
<div  v-else  >
 <v-card
  :elevation="hover ? 16 : 8"
  :class="{ 'on-hover': hover }"
  class="rounded-xl"
  
   color="#1569EF"  >
<v-img
  width="30%"
  :src="Man"
>
</v-img>
<font color="#fff" >Diseñador de Productos</font>


    </v-card>

  </div>


</v-hover>
    </v-col>
 




<v-col>
<h1>Sobre Mí</h1>
<v-hover
        v-slot="{ hover }"
        open-delay="200"
      >
<div  v-if="hover"    >
  <v-card
  :elevation="hover ? 16 : 8"
  :class="{ 'on-hover': hover }"
   color="#fff" 
   class="rounded-xl" >


<v-img
  width="30%"
  :src="CV"
>
</v-img>

  <font color="#000">Me llamo Carlos Delgado, focalizo los 
    resultados de mercado diseñando centrado en el usuario.
</font>

<font color="#000">
Trabajo por SCRUM y Design Thinking
</font>


    </v-card>
</div>

<div  v-else  >
 <v-card
  :elevation="hover ? 16 : 8"
  :class="{ 'on-hover': hover }"
   color="#1569EF" 
   class="rounded-xl" >


<v-img
  width="30%"
  :src="CV"
>
</v-img>

  <font color="#fff" >Me llamo Carlos Delgado, focalizo los resultados de mercado diseñando centrado en el usuario.

Trabajo por SCRUM y Design Thinking


</font>
    </v-card>

  </div>

    </v-hover>
    </v-col>

  </v-row>



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
import portafolio from '@/assets/recursosVisuales/portafolio.png'
import d3 from '@/assets/recursosVisuales/3d.png'

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
