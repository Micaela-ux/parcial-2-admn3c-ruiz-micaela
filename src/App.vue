<template>
  <v-app>
  
    <v-navigation-drawer v-model="drawer" app>
      <v-list>
        <v-list-item link to="/">
          <v-list-item-icon>
            <v-icon>mdi-view-list</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Mi menú semanal</v-list-item-title>
        </v-list-item>

        <v-list-item link to="/ingresar">
          <v-list-item-icon>
            <v-icon>mdi-plus-circle</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Ingresar un menú</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    
    <v-app-bar app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title><span>MS</span></v-toolbar-title>
    </v-app-bar>

    <v-main class="text-center">
      
      <v-container class="header">
        <h1>Mi menú semanal</h1>
      
      </v-container>

      <v-container class="contenedor">
        <router-view/>
      </v-container>
  
    </v-main>

    <v-footer>
      <v-container>
        <v-row>
          <v-col
            cols="12"
            md="6"
          >
              <p> Copyright 2023 Menú Semanal. Todos los derechos reservados.</p>
          </v-col>
          <v-col
            cols="12"
            md="6"
          >
              <p class="text-end">
                  Diseñado por 
                <strong>Ruiz Micaela</strong> 
              </p>
          </v-col>
          </v-row>
      </v-container>
    </v-footer>

  </v-app>
</template>

<script>

  export default {
    name: 'App',

    data: () => ({
        drawer: false,
       
    }),
  };

</script>

<style>

  .header{
    padding: 5%;
    background-color: #8c0202;
    text-align: center;
    color: white;
  }
  .contenedor{
    padding:15px;
  }

</style>
