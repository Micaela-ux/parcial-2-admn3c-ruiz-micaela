<template>
<v-app>
  <div class="about pt-4">
    <h1>Ingresar un menú</h1>
  </div>

    <IngresarMenu></IngresarMenu>
 </v-app>
</template>


<script>
import IngresarMenu from '@/components/IngresarMenu.vue';

export default {
  name: 'HomeView',
  components: {
    IngresarMenu,
  }
}
</script>
