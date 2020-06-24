<template>
    <v-layout justify-center align-center>
        <v-flex xs12 sm8 md8 lg8 xl8>
            <v-card elevation="12">
                <v-layout>
                    <v-flex xs1 sm6 md6 lg6 xl6  ocultar-div>
                        <v-img  :src="require('@/assets/registro.png')" alt=""></v-img>
                    </v-flex>
                    <v-flex xs12 sm12 md12 lg12 xl12>
                        <v-card-text>
                            <v-content class="mx-12 mb-4">
                                <div  class="text-center my-12">
                                <h1 class=" subheading grey--text"> <span>Entrar</span></h1> 
                                 </div>
                                    <v-text-field label="Email" type="password"></v-text-field>
                                     <v-text-field label="Password"></v-text-field>
                                       <div class="text-center">
                                           <v-btn color="primary my-12">Entrar</v-btn>
                                       </div>
                                   <v-content> Deseas 
                                      <a href=""> Registrarte? </a>  
                                   </v-content> 
                            </v-content>
                        </v-card-text>
                    </v-flex>
                </v-layout>
            </v-card>
        </v-flex>
    </v-layout>
</template>
<style>
@media screen and (max-width: 700px) {
.ocultar-div{
display:none;
}
}
</style>