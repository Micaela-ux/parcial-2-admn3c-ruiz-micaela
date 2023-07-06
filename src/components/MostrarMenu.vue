<template>
 <div>

  <v-card
      v-for="item in local"
      :key="item.id"
  >
    <v-card-text>
      <div>Horario: {{item.horario}} hs.</div>
      <p class="text-h4 text--primary">
        {{item.dia}}
      </p>
      <div class="text--primary">
       Menú: {{item.menu}}
      </div>
      <div class="text--primary">
       Postre: {{item.postre}}
      </div>
    </v-card-text>
    <v-card-actions class="btn-delete">
        <v-btn
          color="error"
          class="mt-2"
          @click="eliminar(item)"
        >
          Eliminar
        </v-btn>
      </v-card-actions>
  </v-card>

 </div>
</template>


<script>

  export default {

    data: () => ({
      
      name: 'MostrarMenu',

      local:[],

    }),

    mounted:function(){
      console.log("se monto");
      this.ver_local();
    },

    methods:{
      ver_local:function(){
        
        if(localStorage.dato){
          this.local=JSON.parse(localStorage.getItem("dato"));     
        }
      },

      eliminar(x) {
        this.local.splice(x, 1);
        this.saveDato();
      },

      saveDato() {
      const parsed = JSON.stringify(this.local);
      localStorage.setItem('dato', parsed);
      }

    }

  }
</script>

<style>
  .btn-delete{
    display: flex;
    padding: 8px;
    justify-content: flex-end;
    align-items: center;
  }
  
</style>