<template>
    <v-container>

      <IngresarMenu></IngresarMenu>

    </v-container>
</template>

<script>
  import IngresarMenu from '@/components/IngresarMenu';

  export default {
    name: 'IngresarView',
    
    components: {
      IngresarMenu,
    }
  }
</script>

