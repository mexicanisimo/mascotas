<template>

    <div class="container">
    <div class="row">
              <v-col
        v-for="i in mascotas"
        :key="i.oid"
        cols="12"
        sm="4"
        class="my-2"
      >

  <v-card
    max-width="344"
    max-height="430"
    class="mx-auto"
  >
    <v-list-item>
    
      <v-list-item-content>
        <v-list-item-title class="headline text-center font-weight-black  titulos--text"> SE BUSCA</v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-img
      src="../assets/perrito.jpg"
      height="194"
    ></v-img>

    <v-card-text height="200"> 
     <v-list-item-subtitle class="text-center font-weight-black  light-blue--text"> Raza:{{i.Raza }} Sexo:{{i.Sexo}}</v-list-item-subtitle>
          <div class="text-subtitle">Descripción:</div>
           <div class="text-subtitle2">{{i.Descripcion}}</div>
            
    </v-card-text>

    <v-card-actions>
      <v-btn
        text
        color="deep-purple accent-4"
      >
      Reclamar
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
     data: () => ({
        mascotas:[
            {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            },
             {
                Ubicacion:'Colonial el salvador',
                Raza: 'Rotwailer',
                Especie:'Canino',
                Sexo:'Hembra',
                Descripcion:'Responde al nombre de lucy tiene 2 año de edad lleva un collar'
            }
        ]
         }),
    }

</script>