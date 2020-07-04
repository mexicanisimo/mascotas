<template>

    <div class="container elevation-2 my-6 ">
      <h1 class="text-center" > Mascotas encontradas</h1>
    <div class="row">
              <v-col
        v-for="i in mascotas"
        :key="i.oid"
        cols="12"
        sm="4"
        class="my-2"
      >

  <v-card
    max-width="370"
    height="450"
    class="mx-auto"
  >
   

    <v-img
      src="../assets/perrito.jpg"
      height="194"
    ></v-img>

    <v-card-text height="300"> 
      <div class="headline text-center font-weight-black  ">  Encontrado</div>
  <v-divider class="my-2"></v-divider>
     <v-list-item-subtitle class="font-weight-black "> Raza:{{i.Raza }} Sexo:{{i.Sexo}}</v-list-item-subtitle>
     
          <div class="font-weight-medium  titulos--text"> Lugar donde fue encontrado:{{i.Municipio }} Colonia:{{i.Colonia }} Calles:{{i.Ubicacion}}</div>
          <v-divider class="my-2"></v-divider>
          <div class="subtitle font-weight-medium econtrado--text">Descripción: {{i.Descripcion}}</div>
   
    </v-card-text>

    <v-card-actions>
      <v-btn
        text
        color="deep-purple accent-4" 
      >
      Contactar
      </v-btn>
      <v-btn
        text
        color="deep-purple accent-4"
      >
      
      </v-btn>
    
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-share-variant</v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>


         
     
     </v-col>
    </div>
      <div class="text-center">
    <v-pagination
      v-model="page"
      :length="4"
      circle
    ></v-pagination>
  </div>
    </div>
</template>
<style>

</style>
<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>

<script>
export default {
  methods:{
    
  },
     data: () => ({
       total:0,
       page:0,
       pages:0,
       elementoporpagina:6,
        mascotas:[
            {
                Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                 Municipio:'Puebla',
                Colonia:'Colonial el salvador',
                Ubicacion:'Calle 3 poniente 4 norte',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            }
        ]
         }),
    }

</script>