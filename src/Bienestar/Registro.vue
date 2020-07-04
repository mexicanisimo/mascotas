<template>
  <v-data-table
    :headers="headers"
    :items="desserts"
    sort-by="Autor"
    class=" mx-4 my-4"
  >
    <template v-slot:top>
      <v-toolbar flat color="white">
        <v-toolbar-title>Negocios</v-toolbar-title>
        <v-divider
          class="mx-4"
          inset
          vertical
        ></v-divider>
        <v-spacer></v-spacer>
        <v-dialog v-model="dialog" max-width="530px">
          <template v-slot:activator="{ on }">
            <v-btn color="primary" dark class="mb-2" v-on="on">Registrar</v-btn>
          </template>
          <v-card>
            <v-card-title>
              <span class="headline">{{ formTitle }}</span>
            </v-card-title>

            <v-card-text>
              <v-container>
                <v-row>
                     <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step :complete="e1 > 1" step="1">Negocio</v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step :complete="e1 > 2" step="2">Dueño</v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="3">Veterinario</v-stepper-step>
    </v-stepper-header>

    <v-stepper-items>
      <v-stepper-content step="1">
        <v-card
          class="mb-12"
          max-width="500px"
        >
        <v-row>
<v-col cols="12" sm="6" md="6">
                    <v-text-field v-model="editedItem.negocio" label="Nombre negocio" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="6" >
                    <v-select
                    :items="negocio"
                    label="Tipo de negocio"
                    ></v-select>
                  </v-col>
                   <v-col cols="12" sm="6" md="6">
                    <v-select
                    :items="estados"
                    label="Estado"
                    ></v-select>
                  </v-col>
                  <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.municipio" label="Municipio" type="text"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.colonia" label="Colonia" type="text"></v-text-field>
                  </v-col>
                  
                  <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Dirección" type="text"></v-text-field>
                  </v-col>
                 <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.telefono" label="Teléfono" type="text"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.link" label="Nombre en redes sociales" type="text"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.correo" label="Correo" type="text"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="6" >
                    <v-select
                    v-model="editedItem.anios"
                    :items="anios"
                    label="Años operando"
                    ></v-select>
                  </v-col>
                    <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.Descuento" label="Horario de atención"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="6" >
                    <v-select
                    v-model="editedItem.anios"
                    :items="semana"
                    label="Dias "
                    ></v-select>
                  </v-col>
                  <v-col cols="12" sm="12" >
                    <v-textarea
                    name="input-7-1"
                    filled
                    label="Actividades que realiza"
                    auto-grow
                    v-model="editedItem.actividades"
                  ></v-textarea>
                  </v-col>
                  <v-col cols="12" sm="6" >
                    <v-select
                    :items="estatus"
                    label="Estatus"
                    v-model="editedItem.estatus"
                    ></v-select>
                  </v-col>      
                  <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.Descuento" label="Capacidad de albergar"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="12" >
                    <v-textarea
                    name="input-7-1"
                    filled
                    label="Dictamen bienestar"
                    auto-grow
                  ></v-textarea>
                  </v-col>
                   <v-col cols="12" sm="12" >
                    <v-textarea
                    name="input-7-1"
                    filled
                    label="Descripción de servicios"
                    auto-grow
                  ></v-textarea>
                  </v-col>

                  <v-col cols="12" sm="12" >
                    <v-text-field v-model="editedItem.Descuento" label="Constancia de algun curso"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="12" >
                    <v-text-field v-model="editedItem.Descuento" label="Pertenece a alguna asociación"></v-text-field>
                  </v-col>
                  
                  <!-- Subir archivo -->
                  <v-col cols="12" sm="6" >
                  <v-file-input
                    label="Subir fotografia"
                    filled
                    prepend-icon="fa fa-image"
                  ></v-file-input>
                  </v-col>
                   <v-col cols="12" sm="6" >
                  <v-file-input
                    label="Subir fotografia"
                    filled
                    prepend-icon="fa fa-image"
                  ></v-file-input>
                  </v-col>
                  <v-divider
              
                  inset
                  vertical
                ></v-divider>
                  <v-col cols="12" sm="12">
                       <div class="text-subtitle text-center font-weight-black">Acreditaciones</div>
                  </v-col>
                   <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.colonia" label="Nombre acreditación" type="text"></v-text-field>
                  </v-col>
                  
                  <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Instituto" type="text"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="12">
                       <div class="text-subtitle text-center font-weight-black">Especialidades</div>
                  </v-col>
                   <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.colonia" label="Nombre especialidad" type="text"></v-text-field>
                  </v-col>
                  
                  <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Descripción" type="text"></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="12">
                       <div class="text-subtitle text-center font-weight-black">Criaderos</div>
                  </v-col>
                   <v-col cols="12" sm="6" >
                    <v-text-field v-model="editedItem.colonia" label="Especie" type="text"></v-text-field>
                  </v-col>
                  
                  <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Raza" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Descripción" type="text"></v-text-field>
                  </v-col>
        </v-row>
        </v-card>

        <v-btn
          color="primary"
          @click="e1 = 2"
        >
          Continue
        </v-btn>

        <v-btn text>Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-content step="2">
        <v-card
          class="mb-12"
          width="500px"
        > 
        <v-row>
          <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Nombre" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Apellido paterno" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Apellido materno" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Domicilio" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Telefono" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Correo" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Razón social" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Asociación social inscrito" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="8" > 
                  <v-file-input
                    label="Subir credencial"
                    filled
                    prepend-icon="fa fa-image"
                  ></v-file-input>
                  </v-col>
                  </v-row>
        </v-card>

        <v-btn
          color="primary"
          @click="e1 = 3"
        >
          Continue
        </v-btn>

        <v-btn text>Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-content step="3">
        <v-card
           class="mb-12"
          width="500px"
        > 
        <v-row>
          <v-col cols="12" sm="12">
                  <v-col cols="12" sm="12">
                       <div class="text-subtitle text-center font-weight-black">Datos del veterinario</div>
                  </v-col>
                    <v-text-field v-model="editedItem.direccion" label="Nombre veterinario" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Apellido paterno" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Apellido materno" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Domicilio" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Telefono" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="6">
                    <v-text-field v-model="editedItem.direccion" label="Correo" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Cédula profesional" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Razón social" type="text"></v-text-field>
                  </v-col>
                   <v-col cols="12" sm="12">
                    <v-text-field v-model="editedItem.direccion" label="Asociación social inscrito" type="text"></v-text-field>
                  </v-col>
                    <v-col cols="12" sm="8" > 
                  <v-file-input
                    label="Subir credencial"
                    filled
                    prepend-icon="fa fa-image"
                  ></v-file-input>
                  </v-col>
                  </v-row></v-card>

        <v-btn
          color="primary"
          @click="e1 = 1"
        >
          Continue
        </v-btn>

        <v-btn text>Cancel</v-btn>
      </v-stepper-content>
    </v-stepper-items>
  </v-stepper>
                </v-row>
              </v-container>
            </v-card-text>

            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn color="blue darken-1" text @click="close">Salir</v-btn>
              <v-btn color="blue darken-1" text @click="save">Guardar</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-toolbar>
    </template>
    <template v-slot:item.actions="{ item }">
      <v-icon
        small
        class="mr-2"
        @click="editItem(item)"
      >
        fas fa-edit
      </v-icon>
      <v-icon
        small
        @click="deleteItem(item)"
      >
        far fa-trash-alt
      </v-icon>
    </template>
    <template v-slot:no-data>
      <v-btn color="primary" @click="initialize">Reset</v-btn>
    </template>
  </v-data-table>
</template>
<script>
  export default {
    data: () => ({
      dialog: false,
      estados: ['Puebla', 'Tlaxcala', 'Oaxaca', 'Veracruz'],
      negocio: ['Escuelas adiestramiento', 'Tienda de mascota', 'Estetica', 'Hospitales', 'Criaderos', 'Otro'],
      anios:['1','2','3','4','5','6'],
      estatus:['Activo', 'Inactivo'],
      semana:['Lunes a viernes', 'Lunes a sabado', 'Lunes a domingo'],
      e1:1,
      headers: [
        {
          text: 'Nombre curso',
          align: 'start',
          sortable: false,
          value: 'Nombrecurso',
        },
        { text: 'Nombre autor', value: 'Autor' },
        { text: 'Descripción', value: 'Descripcion' },
        { text: 'Categoría', value: 'Categoria' },
        { text: 'Temario', value: 'Temario' }, 
        { text: 'Precio', value: 'Precio' },
        { text: 'Descuento', value: 'Descuento' },
        { text: 'Estatus', value: 'Estatus' },
        { text: 'Acciones', value: 'actions', sortable: false },
      ],
      desserts: [],
      editedIndex: -1,
      editedItem: {
        Nombrecurso: '',
        Autor: '',
        Descripcion: '',
        Categoria: '',
        Temario: '',
        Precio: '',
        Descuento: '',
        Estatus: '',
        
      },
      defaultItem: {
        Nombrecurso: '',
        Autor: '',
        Descripcion: '',
        Categoria: '',
        Temario: '',
        Precio: '',
        Descuento: '',
        Estatus: '',
      },
    }),

    computed: {
      formTitle () {
        return this.editedIndex === -1 ? 'Establecimiento' : 'Editar'
      },
    },

    watch: {
      dialog (val) {
        val || this.close()
      },
    },

    created () {
      this.initialize()
    },

    methods: {
      initialize () {
        this.desserts = [
          {
            Nombrecurso: 'Frozen Yogurt',
            Autor: 159,
            Descripcion: 6.0,
            Categoria: 'yolo',
            Temario: 24,
            Precio: 4.0,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Ice cream sandwich',
            Autor: 237,
            Descripcion: 9.0,
            Categoria: 'yolo',
            Temario: 37,
            Precio: 4.3,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Eclair',
            Autor: 262,
            Descripcion: 16.0,
            Categoria: 'yolo',
            Temario: 23,
            Precio: 6.0,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Cupcake',
            Autor: 305,
            Descripcion: 3.7,
            Categoria: 'yolo',
            Temario: 67,
            Precio: 4.3,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Gingerbread',
            Autor: 356,
            Descripcion: 16.0,
            Categoria: 'yolo',
            Temario: 49,
            Precio: 3.9,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Jelly bean',
            Autor: 375,
            Descripcion: 0.0,
            Temario: 94,
            Precio: 0.0,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Lollipop',
            Autor: 392,
            Descripcion: 0.2,
            Temario: 98,
            Precio: 0,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Honeycomb',
            Autor: 408,
            Descripcion: 3.2,
            Temario: 87,
            Precio: 6.5,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'Donut',
            Autor: 452,
            Descripcion: 25.0,
            Temario: 51,
            Precio: 4.9,
            Descuento: 'w',
            Estatus: 'w',
          },
          {
            Nombrecurso: 'KitKat',
            Autor: 518,
            Descripcion: 26.0,
            Temario: 65,
            Precio: 7,
            Descuento: 'w',
            Estatus: 'w',
          },
        ]
      },

      editItem (item) {
        this.editedIndex = this.desserts.indexOf(item)
        this.editedItem = Object.assign({}, item)
        this.dialog = true
      },

      deleteItem (item) {
        const index = this.desserts.indexOf(item)
        confirm('Are you sure you want to delete this item?') && this.desserts.splice(index, 1)
      },

      close () {
        this.dialog = false
        setTimeout(() => {
          this.editedItem = Object.assign({}, this.defaultItem)
          this.editedIndex = -1
        }, 300)
      },

      save () {
        if (this.editedIndex > -1) {
          Object.assign(this.desserts[this.editedIndex], this.editedItem)
        } else {
          this.desserts.push(this.editedItem)
        }
        this.close()
      },
    },
  }
</script>