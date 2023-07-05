<template>
  <v-app>
    <v-form @submit.prevent="submit">
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
            <v-select
              v-model="select"
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
              v-model="horario"
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
              v-model="menu"
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
              v-model="postre"
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
  </v-app>
</template>

<script>
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
    
    }),

  } 
</script>