<template>
  <v-app>
 
    <v-content style="background-color: ">
    



  <component :is="componenteActual"></component> 
    </v-content>

  </v-app>
</template>

<script>
//import Toolbar from "./components/Toolbar";
import Footer from "./components/Footer";
import Portafolio from "./components/Portafolio.vue";
import Login from "@/views/Login.vue";
import Registro from "@/views/Registro.vue";
import adopciones from "@/views/adopciones.vue";
// import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    // HelloWorld,

   Footer,
   Portafolio,
   Login,
   Registro,
   adopciones
  
  },

  data: () => ({
   componenteActual: 'adopciones',
  })
};
</script>
<style lang="scss">

</style>