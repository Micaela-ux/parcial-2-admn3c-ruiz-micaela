<template>
<v-app>
  <v-table>
    <thead>
      <tr>
        <th class="text-center">
          Día
        </th>
        <th class="text-center">
          Horario
        </th>
        <th class="text-center">
          Menú
        </th>
        <th class="text-center">
          Postre
        </th>
        <th class="text-center">
          Acciones
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in desserts"
        :key="item.name"
      >
        <td>{{ item.name }}</td>
        <td>{{ item.calories }}</td>
        <td>{{ item.name }}</td>
        <td>{{ item.name }}</td>
        <td>
          <v-btn
            color="error"
            class="mt-2"
            block
            @click="reset"
          >
            Eliminar
          </v-btn>
        </td>
      </tr>
    </tbody>
  </v-table>
 
 </v-app>
</template>


<script>

  export default {

    data () {
      return {

      titulo: "Mi menú semanal",

        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
          },
          {
            name: 'Eclair',
            calories: 262,
          },
          {
            name: 'Cupcake',
            calories: 305,
          },
          {
            name: 'Gingerbread',
            calories: 356,
          },
          {
            name: 'Jelly bean',
            calories: 375,
          },
          {
            name: 'Lollipop',
            calories: 392,
          },
          {
            name: 'Honeycomb',
            calories: 408,
          },
          {
            name: 'Donut',
            calories: 452,
          },
          {
            name: 'KitKat',
            calories: 518,
          },
        ],
      }
    },
  }
</script>

<style>
  .header{

    padding: 5%;
    background-color: #8c0202;
    text-align: center;
    color: white;

  }
</style>