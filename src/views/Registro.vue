<template>
    <v-layout justify-center align-center> 
        <v-flex xs12 sm8 md8 lg6 xl6>
            <v-card elevation="12">
                <v-layout>
                    <v-flex xs1 sm6 md6 lg6>
                        <v-img  :src="require('@/assets/login.png')" alt=""></v-img>
                    </v-flex>
                    <v-flex xs12 sm12 md12 lg12 xl12>
                        <v-card-text>
                            <v-content class="mx-10 mb-4">
                                 <div  class="text-center my-5">
                          <h1 class=" subheading grey--text"> <span>Registro</span></h1> 
                         </div>
                      <v-text-field label="Ussername"></v-text-field>
                      <v-text-field label="Email" type="password"></v-text-field>
                      <v-text-field label="Password"></v-text-field>
                      <v-text-field label="Password" type="password"></v-text-field>
                      <div class="text-center">
                             <v-btn color="primary">Registro</v-btn>
                      </div>
                      <v-content class="my-2"> Deseas 
                        <a href=""> Entrar? </a>  
                            </v-content>
                          </v-content>
                        </v-card-text>
                    </v-flex>
                </v-layout>
            </v-card>
        </v-flex>
    </v-layout>
</template>