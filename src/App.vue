<template>
  <v-app>
    <v-app-bar
      app
      color="ligth"
      white
    >
      <div class="d-flex align-center">
        <span>MS</span>
      </div>

      <v-spacer>
    
      </v-spacer>

      <v-btn
        text
      >
        <span class="mr-2">Iniciar sesión</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main class="text-center">
        
      
          <v-list-item-content>
              <v-list-item-title>
                <router-link to="/">
                Home
                </router-link>
              </v-list-item-title>
            </v-list-item-content>

            <v-list-item-content>
              <v-list-item-title>
                <router-link to="/ingresar">
                 Ingresar
                </router-link>
              </v-list-item-title>
            </v-list-item-content>
          

         <!-- <v-list-item link to="/ingresar">
            <v-list-item-title>Ingresar</v-list-item-title>
          </v-list-item>
-->

       
    </v-main>

   

    <v-container>
       <router-view/>
    </v-container>

  </v-app>
</template>

<script>


export default {
  name: 'App',

  data: () => ({
     //
  }),
};
</script>

