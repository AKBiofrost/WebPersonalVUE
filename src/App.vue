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



<cabecera></cabecera>

<v-col justify="center"  >

<div  class="titulo"  >
<h1 > Alexander K.Biofröst   </h1>

</div>

<div  class="Subtitulo"  >
<h2 > Diseñador de Productos  </h2>
</div>


<redes></redes>


</v-col>

<tableros></tableros>





</v-col>








</v-card>
</v-main>
  </v-app>
</template>

<script>
import { Bubble } from 'vue-burger-menu' 

import cabecera from '@/components/cabecera.vue'
import tableros from '@/components/tableros.vue'
import redes from '@/components/redesSociales.vue'

export default {
  name: 'App',

  data: () => ({
    redes:redes,
    tableros:tableros,
    cabecera:cabecera,
    

    //
  }),
components: {
        Bubble, // Register your component,
        cabecera,
        tableros,
        redes

    }

};
</script>



<style lang="scss" scoped  >


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
