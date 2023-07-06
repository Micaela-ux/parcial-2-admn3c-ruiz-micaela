<template>
  <v-form @submit.prevent>
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <v-select
            v-model="form_data.dia"
            :items="items"
            :rules="[v => !!v || 'Seleccione un día.']"
            label="Día: "
            required
          ></v-select>
        </v-col>

        <v-col
          cols="12"
          md="6"
        >
          <v-text-field
            v-model="form_data.horario"
            :rules="obligatorio"
            label="Horario: "
            required
          ></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col
          cols="12"
          md="6"
        >
          <v-text-field
            v-model="form_data.menu"
            :rules="obligatorio"
            label="Menú: "
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          md="6"
        >
          <v-text-field
            v-model="form_data.postre"
            :rules="obligatorio"
            label="Postre: "
            required
          ></v-text-field>
        </v-col>
      </v-row>

      <v-row>
        <v-col
        cols="12"
        >
          <v-btn
              @click="agregar(form_data)"
            >
              Agregar
            </v-btn>
        </v-col>
      </v-row>

    </v-container>
  </v-form>
</template>

<script>
  
  var menus = [];

  export default {
    data: () => ({
      name: 'IngresarMenu',
      select: null,
      items: [
        'Lunes',
        'Martes',
        'Miércoles',
        'Jueves',
        'Viernes',
        'Sabádo',
        'Domingo',
      ],

      horario: '',
      menu: '',
      postre: '',

      obligatorio: [
        value => {
          if (value) return true
          return 'Completar, campo obligatorio.'
        },
      ],

      form_data:{
        dia: "",
        horario: "",
        menu: "",
        postre: "",
      },

    }),

    methods:{
      agregar:function(form_data){
        if(!localStorage.dato){
          menus=[];
        }else{
          menus=JSON.parse(localStorage.getItem("dato"));
        }

        menus.push(form_data);
        localStorage.setItem("dato",JSON.stringify(menus));
      
        this.$router.push('/');

      }

    },
	}
</script>