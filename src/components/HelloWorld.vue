<!-- <h2 class="mb-5  mt-5">
                        <span>Conoce nuestras opciones </span>
                </h2>
                </div>

            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-lg-12">
                        <div class="row row-grid">
                            <div class="col-lg-4">
                                <card class="border-0" hover shadow body-classes="py-5">
                                    <icon name="ni ni-check-bold" type="primary" rounded class="mb-4">
                                    </icon>
                                    <h6 class="text-primary text-uppercase">Salud para mascotas</h6>
                                    <p class="description mt-3">Veterinarias y hospitales registrados. 

                                    </p>
                                    <div>
                                        <badge type="primary" rounded>Veterinarias</badge>
                                        <badge type="primary" rounded>Hospitales</badge>
                                        <badge type="primary" rounded>Veterinarios</badge>
                                    </div>
                                    <base-button tag="a" href="#" type="primary" class="mt-4">
                                        Ver Catálogo
                                    </base-button>
                                </card>
                            </div>
                            <div class="col-lg-4">
                                <card class="border-0" hover shadow body-classes="py-5">
                                    <icon name="ni ni-map-big" type="success" rounded class="mb-4">
                                    </icon>
                                    <h6 class="text-success text-uppercase">Asociaciones  </h6>
                                    <p class="description mt-3">Asociaciones de protección animal en puebla.
 <div>
                                        <badge type="success" rounded>Asociaciones</badge>
                                        <badge type="success" rounded>Brigadas</badge>
                                        <badge type="success" rounded>Instituciones</badge>
                                    </div>
                                    <base-button tag="a" href="#" type="success" class="mt-4">
                                        Ver Catálogo
                                    </base-button>
                                </card>
                            </div>
                            <div class="col-lg-4">
                                <card class="border-0" hover shadow body-classes="py-5">
                                    <icon name="ni ni-ruler-pencil" type="warning" rounded class="mb-4">
                                    </icon>
                                    <h6 class="text-warning text-uppercase">Escuelas de adiestramiento</h6>
                                    <p class="description mt-3">Visualiza las escuelas de adiestramiento en puebla  </p>
                                    <div>
                                        <badge type="warning" rounded>Escuela</badge>
                                        <badge type="warning" rounded>Internado</badge>
                                       
                                    </div>
                                    <base-button tag="a" href="#" type="warning" class="mt-4">
                                        Ver Catálogo
                                    </base-button>
                                </card>
                            </div>
                        </div>
                    </div>
                  </div>
             
               <div class="row justify-content-center mt-5">
                    <div class="col-lg-12">
                        <div class="row row-grid">
                            <div class="col-lg-4">
                                <card class="border-0" hover shadow body-classes="py-5">
                                    <icon name="ni ni-scissors" type="default" rounded class="mb-4">
                                    </icon>
                                    <h6 class="text-default text-uppercase">Esteticas</h6>
                                    <p class="description mt-3">¿Estética para tu mascota? <div>
                                        <badge type="default" rounded>Look</badge>
                                        </div>
                                    <base-button tag="a" href="#" type="default" class="mt-4">
                                        Ver Catálogo
                                    </base-button>
                                </card>
                            </div>
                            <div class="col-lg-4">
                                <card class="border-0" hover shadow body-classes="py-5">
                                    <icon name="ni ni-istanbul" type="info" rounded class="mb-4">
                                    </icon>
                                    <h6 class="text-info text-uppercase">Criadores</h6>
                                    <p class="description mt-3">Visualiza criaderos autorizados en puebla <div>
                                            </div>
                                    <base-button tag="a" href="#" type="info" class="mt-4">
                                         Ver Catálogo
                                    </base-button>
                                </card>
                            </div>
                            <div class="col-lg-4">
                                <card class="border-0" hover shadow body-classes="py-5">
                                    <icon name="ni ni-planet" type="danger" rounded class="mb-4">
                                    </icon>
                                    <h6 class="text-danger text-uppercase">Exhibición</h6>
                                    <p class="description mt-3">Visualiza los negocios con exhibición de mascotas.<div>
                       
                                    </div>
                                    <base-button tag="a" href="#" type="danger" class="mt-4">
                                        Ver Catálogo
                                    </base-button>
                                </card>
                            </div>
                        </div>
                    </div>
                    </div> 
                  </div>

     <section class="section section-components pb-0" id="section-components">
     <div class="container">

    <div class="row">
          <div class="col-md-4">
            <base-button block type="primary" class=" mb-3" @click="modals.modal1 = true">
                Registro de mascotas
            </base-button>
            <modal :show.sync="modals.modal1">
                <h6 slot="header" class="modal-title" id="modal-title-default">Registro de mascotas </h6>
                         
                    <p>Llene los siguientes campos.</p>
               
            <div class="mb-3">
                <small class="text-uppercase font-weight-bold">Datos de mascota</small>
            </div>
                 <base-input placeholder="Nombre">
                </base-input>
                <base-input placeholder="Acto de adopción">
                </base-input>
                <div class="row">  
                   <div class="col-md-6">
                       <base-input placeholder="Especie">
                </base-input>
                   </div>
                   <div class="col-md-6">
                       <base-input placeholder="Raza">
                </base-input>
                   </div>
                </div>
                <div class="row">  
                   <div class="col-md-6">
                       <base-input placeholder="Sexo">
                </base-input>
                   </div>
                   <div class="col-md-6">
                       <base-input placeholder="Color">
                </base-input>
                   </div>
                </div>
                <base-input placeholder="Señas Particulares">
                </base-input>
                <base-input placeholder="Modo identificiacion o número">
                </base-input>
                <base-input placeholder="Fecha nacimiento">
                </base-input>
                <base-input placeholder="Enfermedad">
                </base-input>
                <base-input placeholder="Foto">
                </base-input>
                < slot="footer">
                    <base-button type="primary">Registrar</base-button>
                    <base-button type="link" class="ml-auto" @click="modals.modal1 = false">Cerrar
                    </base-button>
                </template>
            </modal>
        </div>
        
        <div class="col-md-4">
            <base-button block type="warning" class=" mb-3" @click="modals.modal2 = true">
                Denuncia
            </base-button>

            <modal :show.sync="modals.modal2"
                   gradient="danger"
                   modal-classes="modal-danger modal-dialog-centered">
                <h6 slot="header" class="modal-title" id="modal-title-notification">Denuncia</h6>

                <div class="py-3 text-center">
                   
                    <h4 class="heading mt-4">Denuncia Maltrato animal</h4>
                    <p>Llene los siguientes campos.</p>
               
            <div class="mb-3">
                <small class="text-uppercase font-weight-bold">Nombre</small>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <base-input placeholder="Nombre">
                    </base-input>
                    <base-input placeholder=" Primer Apellido">
                    </base-input>
                    <base-input placeholder="Segundo Apellido">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                    <base-input placeholder="Telefono">
                    </base-input>
                    <base-input placeholder="Correo">
                    </base-input>
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Denuncia correspondiete a:</small>
                    </div>
                    <base-input placeholder="Nombre denunciado">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                   <base-input class="mb-3">
                                    <textarea class="form-control form-control-alternative" name="name" rows="4"
                                              cols="80" placeholder="Describe los hechos"></textarea>
                    </base-input>
                     
                    
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Pruebas</small>
                     <p>Si tiene un enlace capturado en redes sociales envie link.</p>
                    </div>
                    <base-input placeholder="Link 1">
                    </base-input>
                    <base-input placeholder="Link 2">
                    </base-input>
                    <base-input placeholder="Link 3 ">
                    </base-input>
                    <base-input placeholder="Sube archivo">
                    </base-input>
                     <base-checkbox>
                                Autoriza que llegue notificaciones en su correo y en su Domicilio.
                            </base-checkbox>
                </div>
                </div>

               
                </div>

                < slot="footer">
                    <base-button type="white">Enviar Denuncia</base-button>
                    <base-button type="link"
                                 text-color="white"
                                 class="ml-auto"
                                 @click="modals.modal2 = false">
                        Cancelar
                    </base-button>
                </template>
            </modal>
        </div>
        

        <div class="col-md-4">
            <base-button block type="defaul" class=" mb-3" @click="modals.modal1 = true">
                Hospitales
            </base-button>
            <modal :show.sync="modals.modal1">
                <h6 slot="header" class="modal-title" id="modal-title-default">Registro de hospitales</h6>


                < slot="footer">
                    <base-button type="primary">Save changes</base-button>
                    <base-button type="link" class="ml-auto" @click="modals.modal1 = false">Close
                    </base-button>
                </template>
            </modal>
        </div>
    </div>


 <div class="row">
         <div class="col-md-4">
            <base-button block type="primary" class=" mb-3" @click="modals.modal2 = true">
                Registro de mascota.
            </base-button>

            <modal :show.sync="modals.modal2"
                   gradient="danger"
                   modal-classes="modal-danger modal-dialog-centered">
                <h6 slot="header" class="modal-title" id="modal-title-notification">Registro de mascota</h6>

                <div class="py-3 text-center">
                   
                    <h4 class="heading mt-4">Denuncia Maltrato animal</h4>
                    <p>Llene los siguientes campos.</p>
               

            <div class="mb-3">
                <small class="text-uppercase font-weight-bold">Nombre</small>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <base-input placeholder="Nombre">
                    </base-input>
                    <base-input placeholder=" Primer Apellido">
                    </base-input>
                    <base-input placeholder="Segundo Apellido">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                    <base-input placeholder="Telefono">
                    </base-input>
                    <base-input placeholder="Correo">
                    </base-input>
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Denuncia correspondiete a:</small>
                    </div>
                    <base-input placeholder="Nombre denunciado">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                   <base-input class="mb-3">
                                    <textarea class="form-control form-control-alternative" name="name" rows="4"
                                              cols="80" placeholder="Describe los hechos"></textarea>
                    </base-input>
                     
                    
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Pruebas</small>
                     <p>Si tiene un enlace capturado en redes sociales envie link.</p>
                    </div>
                    <base-input placeholder="Link 1">
                    </base-input>
                    <base-input placeholder="Link 2">
                    </base-input>
                    <base-input placeholder="Link 3 ">
                    </base-input>
                    <base-input placeholder="Sube archivo">
                    </base-input>
                     <base-checkbox>
                                Autoriza que llegue notificaciones en su correo y en su Domicilio.
                            </base-checkbox>
                </div>
                </div>

               
                </div>

                < slot="footer">
                    <base-button type="white">Enviar Denuncia</base-button>
                    <base-button type="link"
                                 text-color="white"
                                 class="ml-auto"
                                 @click="modals.modal2 = false">
                        Cancelar
                    </base-button>
                </template>
            </modal>
        </div>
        <div class="col-md-4">
            <base-button block type="warning" class=" mb-3" @click="modals.modal2 = true">
                Denuncia
            </base-button>

            <modal :show.sync="modals.modal2"
                   gradient="danger"
                   modal-classes="modal-danger modal-dialog-centered">
                <h6 slot="header" class="modal-title" id="modal-title-notification">Denuncia</h6>

                <div class="py-3 text-center">
                   
                    <h4 class="heading mt-4">Denuncia Maltrato animal</h4>
                    <p>Llene los siguientes campos.</p>
               

            <div class="mb-3">
                <small class="text-uppercase font-weight-bold">Nombre</small>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <base-input placeholder="Nombre">
                    </base-input>
                    <base-input placeholder=" Primer Apellido">
                    </base-input>
                    <base-input placeholder="Segundo Apellido">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                    <base-input placeholder="Telefono">
                    </base-input>
                    <base-input placeholder="Correo">
                    </base-input>
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Denuncia correspondiete a:</small>
                    </div>
                    <base-input placeholder="Nombre denunciado">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                   <base-input class="mb-3">
                                    <textarea class="form-control form-control-alternative" name="name" rows="4"
                                              cols="80" placeholder="Describe los hechos"></textarea>
                    </base-input>
                     
                    
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Pruebas</small>
                     <p>Si tiene un enlace capturado en redes sociales envie link.</p>
                    </div>
                    <base-input placeholder="Link 1">
                    </base-input>
                    <base-input placeholder="Link 2">
                    </base-input>
                    <base-input placeholder="Link 3 ">
                    </base-input>
                    <base-input placeholder="Sube archivo">
                    </base-input>
                     <base-checkbox>
                                Autoriza que llegue notificaciones en su correo y en su Domicilio.
                            </base-checkbox>
                </div>
                </div>

               
                </div>

                <slot="footer">
                    <base-button type="white">Enviar Denuncia</base-button>
                    <base-button type="link"
                                 text-color="white"
                                 class="ml-auto"
                                 @click="modals.modal2 = false">
                        Cancelar
                    </base-button>
                </template>
            </modal>
        </div>
        <div class="col-md-4">
            <base-button block type="default" class=" mb-3" @click="modals.modal3 = true">
                Form
            </base-button>

            <modal :show.sync="modals.modal3"
                   body-classes="p-0"
                   modal-classes="modal-dialog-centered modal-sm">
                <card type="secondary" shadow
                      header-classes="bg-white pb-5"
                      body-classes="px-lg-5 py-lg-5"
                      class="border-0">
                 
                        <div class="text-muted text-center mb-3">
                            <small>Sign in with</small>
                        </div>
                        <div class="btn-wrapper text-center">
                            <base-button type="neutral">
                                <img slot="icon" src="img/icons/common/github.svg">
                                Github
                            </base-button>

                            <base-button type="neutral">
                                <img slot="icon" src="img/icons/common/google.svg">
                                Google
                            </base-button>
                        </div>
                    </template>
                   
                        <div class="text-center text-muted mb-4">
                            <small>Or sign in with credentials</small>
                        </div>
                        <form role="form">
                            <base-input alternative
                                        class="mb-3"
                                        placeholder="Email"
                                        addon-left-icon="ni ni-email-83">
                            </base-input>
                            <base-input alternative
                                        type="password"
                                        placeholder="Password"
                                        addon-left-icon="ni ni-lock-circle-open">
                            </base-input>
                            <base-checkbox>
                                Remember me
                            </base-checkbox>
                            <div class="text-center">
                                <base-button type="primary" class="my-4">Sign In</base-button>
                            </div>
                        </form>
                    </template>
                </card>
            </modal>
        </div>
    </div>

  <div class="row">
         <div class="col-md-4">
            <base-button block type="primary" class=" mb-3" @click="modals.modal2 = true">
                Registro de mascota.
            </base-button>

            <modal :show.sync="modals.modal2"
                   gradient="danger"
                   modal-classes="modal-danger modal-dialog-centered">
                <h6 slot="header" class="modal-title" id="modal-title-notification">Registro de mascota</h6>

                <div class="py-3 text-center">
                   
                    <h4 class="heading mt-4">Denuncia Maltrato animal</h4>
                    <p>Llene los siguientes campos.</p>
               

            <div class="mb-3">
                <small class="text-uppercase font-weight-bold">Nombre</small>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <base-input placeholder="Nombre">
                    </base-input>
                    <base-input placeholder=" Primer Apellido">
                    </base-input>
                    <base-input placeholder="Segundo Apellido">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                    <base-input placeholder="Telefono">
                    </base-input>
                    <base-input placeholder="Correo">
                    </base-input>
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Denuncia correspondiete a:</small>
                    </div>
                    <base-input placeholder="Nombre denunciado">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                   <base-input class="mb-3">
                                    <textarea class="form-control form-control-alternative" name="name" rows="4"
                                              cols="80" placeholder="Describe los hechos"></textarea>
                    </base-input>
                     
                    
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Pruebas</small>
                     <p>Si tiene un enlace capturado en redes sociales envie link.</p>
                    </div>
                    <base-input placeholder="Link 1">
                    </base-input>
                    <base-input placeholder="Link 2">
                    </base-input>
                    <base-input placeholder="Link 3 ">
                    </base-input>
                    <base-input placeholder="Sube archivo">
                    </base-input>
                     <base-checkbox>
                                Autoriza que llegue notificaciones en su correo y en su Domicilio.
                            </base-checkbox>
                </div>
                </div>

               
                </div>

               slot="footer">
                    <base-button type="white">Enviar Denuncia</base-button>
                    <base-button type="link"
                                 text-color="white"
                                 class="ml-auto"
                                 @click="modals.modal2 = false">
                        Cancelar
                    </base-button>
                </template>
            </modal>
        </div>
        <div class="col-md-4">
            <base-button block type="warning" class=" mb-3" @click="modals.modal2 = true">
                Denuncia
            </base-button>

            <modal :show.sync="modals.modal2"
                   gradient="danger"
                   modal-classes="modal-danger modal-dialog-centered">
                <h6 slot="header" class="modal-title" id="modal-title-notification">Denuncia</h6>

                <div class="py-3 text-center">
                   
                    <h4 class="heading mt-4">Denuncia Maltrato animal</h4>
                    <p>Llene los siguientes campos.</p>
               

            <div class="mb-3">
                <small class="text-uppercase font-weight-bold">Nombre</small>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <base-input placeholder="Nombre">
                    </base-input>
                    <base-input placeholder=" Primer Apellido">
                    </base-input>
                    <base-input placeholder="Segundo Apellido">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                    <base-input placeholder="Telefono">
                    </base-input>
                    <base-input placeholder="Correo">
                    </base-input>
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Denuncia correspondiete a:</small>
                    </div>
                    <base-input placeholder="Nombre denunciado">
                    </base-input>
                    <base-input placeholder="Domicilio">
                    </base-input>
                   <base-input class="mb-3">
                                    <textarea class="form-control form-control-alternative" name="name" rows="4"
                                              cols="80" placeholder="Describe los hechos"></textarea>
                    </base-input>
                     
                    
                     <div class="mb-3">
                        <small class="text-uppercase font-weight-bold">Pruebas</small>
                     <p>Si tiene un enlace capturado en redes sociales envie link.</p>
                    </div>
                    <base-input placeholder="Link 1">
                    </base-input>
                    <base-input placeholder="Link 2">
                    </base-input>
                    <base-input placeholder="Link 3 ">
                    </base-input>
                    <base-input placeholder="Sube archivo">
                    </base-input>
                     <base-checkbox>
                                Autoriza que llegue notificaciones en su correo y en su Domicilio.
                            </base-checkbox>
                </div>
                </div>

               
                </div>

              slot="footer">
                    <base-button type="white">Enviar Denuncia</base-button>
                    <base-button type="link"
                                 text-color="white"
                                 class="ml-auto"
                                 @click="modals.modal2 = false">
                        Cancelar
                    </base-button>
                </template>
            </modal>
        </div>

        -->
