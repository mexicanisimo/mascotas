<template>
<v-content >

<header>
<nav>
<a href="#"> Nosotros</a>
<a href="#"> Denuncias</a>
<a href="#"> Adopciones</a>
<a href="#"> Contacto</a>
<a href="#"> Registro</a>
<a href="#"> Login</a>
<!-- 
1Veterinarias y hospitales registrados
2 Asociaciones de protección animal en puebla
3 Escuelas de adiestramiento
4 Estética para tu mascota? 
5 Visualiza criaderos autorizados en puebla 
6 Visualiza los negocios con exhibición de mascotas.
7 Registro de mascotas 
8 Denuncia Maltrato animal
9 Personas fisicas 
10 Adopcion
-->
  </nav>
  <section class="textos-header "> 
<h1> ¿Sabías que en méxico es el primer lugar en maltrato animal?</h1>
<h2>Así mismo el 70% de los perros se encuentran en abandono.Inegi</h2>
    <div class="my-2">
    <v-btn rounded color="primary" dark>Registrarse</v-btn>
    </div>
</section>

<div class="wave" style="height: 150px; overflow: hidden;" ><svg viewBox="0 0 500 150" preserveAspectRatio="none" style="height: 100%; width: 100%;"><path d="M0.00,49.98 C273.42,181.08 349.20,-49.98 500.00,49.98 L500.00,150.00 L0.00,150.00 Z" style="stroke: none; fill: #fff;"></path></svg></div>
</header>
<main> 

  <section class="contenedor">
    <h2 class="titulo"> Registrate y accede a nuestras opciones </h2>
  
   <opciones />

  </section>
  <section>
   <div class="contenedor sobre-nosotros">
    <h2 class="titulo"> Servicios</h2>
    <div class="contenedor-sobre-nosotros ">
      <v-flex class="imagen-nosotros  ocultar-div">
       <v-img 
       :src="require('@/assets/mascota2.png')" 
    ></v-img>
       </v-flex>
    <div class="contenido-textos">
      <h3> <span>1</span> Realiza tu Denuncia</h3>
      <p>Realiza tu denuncia, las autoridades se pondran en contacto para el seguimiento de tu caso </p>
      <h3> <span>2</span> Adopta a una mascota</h3>
      <p>Checa nuestra lista de mascotas abandonadas y adopta uno de los animales</p>
      <h3> <span>3</span> Da en Adopción</h3>
      <p>Busca a tu mejor elección para adoptar una mascota</p>
    </div>
    </div>
    </div>
  </section>
  <!--denuncias --> 
    <section>
        <h2 class="text-center"> Nosotros</h2>
   <div class="contenedor sobre-nosotros">
   
    <div class="contenedor-sobre-nosotros ">
    <div class="contenido-textos my-10">
      <h3> <span>1</span> Realiza tu Denuncia</h3>
      <p>Realiza tu denuncia, las autoridades se pondran en contacto para el seguimiento de tu caso </p>
      <h3> <span>2</span> Adopta a una mascota</h3>
      <p>Checa nuestra lista de mascotas abandonadas y adopta uno de los animales</p>
      <h3> <span>3</span> Da en Adopción</h3>
      <p>Busca a tu mejor elección para adoptar una mascota</p>
      <h3> <span>3</span> Da en Adopción</h3>
      <p>Busca a tu mejor elección para adoptar una mascota</p>
    </div>
    
      <v-flex class="imagen-nosotros xs1 sm6 md6 lg6 xl6 ocultar-div">
       <v-img 
       :src="require('@/assets/nosotros.png')" 
    ></v-img>
       </v-flex>
    </div>
    </div>
    
  </section>
  <!-- fin denuncias -->

    <section class="portafolio contenedor">
<div class="contenedor">
  <h2 class="titulo">Instituciones y organizaciones</h2>
  <div class="team-section">
    
    <div class="ps">
      <v-img
       :src="require('@/assets/logo.png')" 
    ></v-img>
    </div>
     <div class="ps">
          <v-img 
       :src="require('@/assets/logo.png')" 
    ></v-img>
    </div>
     <div class="ps">
          <v-img
       :src="require('@/assets/logo.png')" 
    ></v-img>
    </div>
      <div class="ps">
          <v-img
       :src="require('@/assets/logo.png')" 
    ></v-img>
    </div>
  </div>
</div>

  </section>
</main>
  
<section class="textos-header prueba "> 
  <div style="height: 150px; overflow: hidden;" ><svg viewBox="0 0 500 150" preserveAspectRatio="none" style="height: 100%; width: 100%;"><path d="M0.00,49.98 C149.99,150.00 349.20,-49.98 500.00,49.98 L533.01,-27.13 L0.28,0.50 Z" style="stroke: none; fill: #fff;"></path></svg></div>
<h1> ¿Sabías que en méxico es el primer lugar en maltrato animal?</h1>
<h2>Así mismo el 70% de los perros se encuentran en abandono.Inegi</h2>
    <div class="my-2">
    <v-btn rounded color="primary" dark>Registrarse</v-btn>
    </div>
</section>
  <div class="wave" style="height: 150px; overflow: hidden;" ><svg viewBox="0 0 500 150" preserveAspectRatio="none" style="height: 100%; width: 100%;"><path d="M0.00,49.98 C273.42,181.08 349.20,-49.98 500.00,49.98 L500.00,150.00 L0.00,150.00 Z" style="stroke: none; fill: #fff;"></path></svg></div>

</v-content>

</template>

<script>
 import opciones from '@/components/Opciones.vue'
 export default{
   components:{
     opciones,
   },
   data: () => ({
    componenteActual: 'Opciones',
  }),
 }
</script>
<style>
.contenedor{
  padding: 60px 0;
  width: 90%;
  max-width: 1200px;
  margin: auto;
  overflow: hidden;
}

.titulo{
  color: blueviolet;
  font-size:30px ;
  text-align: center;
  margin-bottom: 60px;
}
header{
  width: 100%;
  height: 600px;
background: #00F260;  /* fallback for old browsers */
background: -webkit-linear-gradient(to right, #0575E6, #00F260), url('../assets/animals.png');   /* Chrome 10-25, Safari 5.1-6 */
background: linear-gradient(to right, rgba(5, 118, 230, 0.87), rgb(0, 242, 97)) , url('../assets/animals.png');  /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */


/* background: #03001e; /* fallback for old browsers */
/*  background: -webkit-linear-gradient(to right, #03001e, #7303c0, #ec38bc, #fdeff9), url('../assets/animals.png');  /* Chrome 10-25, Safari 5.1-6 */
/*  background: linear-gradient(to right, #03001e96, #7403c0c9, #ec38bcbe, #03001ed3), url('../assets/animals.png'); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */


background-size: cover ;
background-attachment: fixed;
position: relative;
}


.prueba {
  width: 100%;
  height: 700px;
background: #B38B09;  /* fallback for old browsers */


/* background: #03001e; /* fallback for old browsers */
/*  background: -webkit-linear-gradient(to right, #03001e, #7303c0, #ec38bc, #fdeff9), url('../assets/animals.png');  /* Chrome 10-25, Safari 5.1-6 */
/*  background: linear-gradient(to right, #03001e96, #7403c0c9, #ec38bcbe, #03001ed3), url('../assets/animals.png'); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */


background-size: cover ;
background-attachment: fixed;
position: relative;
}
 nav{
   text-align: right;
   padding: 30px 50px 0 0; 
 }

 nav > a{
   color:#fff !important;
   font-weight: 700;
   text-decoration: none;
   margin-right: 15px;
 }
  nav > a:hover{
   text-decoration: underline;
  }
 header .textos-header{
   display: flex ;
   height: 430px;
   width:100%;
   align-items: center;
   justify-content:center; 
   flex-direction:column ;
   text-align: center;
 }
 .wave{
   position: absolute;
   bottom: 0;
   width: 100%;
 }
 .textos-header h1{
   font-size: 30px;
   color: #fff;
 }
  .textos-header h2{
   font-size: 20px;
   font-weight:300;
   color: #fff;

 }
 .team-section{
   overflow: hidden;
   text-align: center;
 }
 .ps{
   margin-bottom:40px ;
   display: inline-block;
   margin: 0 30px;
   width: 160px;
   height: 160px;
   overflow: hidden;
   border-radius:50% ;
 }
/* nosotros*/
.contenedor-sobre-nosotros{
  display: flex;
  justify-content: space-evenly;
}
.imagen-nosotros{
  width: 48%;
}
.sobre-nosotros .contenido-textos{
  width: 48%;
}
.contenido-textos h3{
  margin-bottom: 15px;
}
.contenido-textos h3 span{
  background: #7403c0c9;
  color: #fff;
  border-radius: 50%;
  display: inline-block;
  text-align: center;
  width: 30px;
  height: 30px;
  padding: 2px;
  background-origin: 0 0 6px 0 rgba(0,0,0,.5);
  margin-right: 5px;
  }
  .contenido-textos p{
    padding: 0px 0px 5px 5px;
  }
@media screen and (max-width: 600px) {
.ocultar-div{
display:none;
}
}
</style>