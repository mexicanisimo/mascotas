<template>
  <v-app>
 
    <v-content style="background-color: ">
    
  <div>
    <v-app-bar
      color="deep-purple accent-4"
      dense
      dark
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Page title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </div>


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
import Encontrados from "@/views/Encontrados.vue";
import Perdidos from "@/views/Perdidos.vue";
import Registros from "@/Bienestar/Registro.vue";

export default {
  name: "App",

  components: {
    // HelloWorld,

   Footer,
   Portafolio,
   Login,
   Registro,
   adopciones,
   Encontrados,
   Perdidos,
   Registros
  
  },

  data: () => ({
   componenteActual: 'Registros',
  })
};
</script>
<style lang="scss">

</style>