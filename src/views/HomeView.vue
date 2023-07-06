<template>
  <v-app>
    <div class="header">
      <h1>Mi menú semanal</h1>
    </div>

      <MostrarMenu></MostrarMenu>
  </v-app>
</template>


<script>
  import MostrarMenu from '@/components/MostrarMenu.vue';

  export default {
    name: 'HomeView',
    components: {
      MostrarMenu,
    }
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

