<template>
  <div>
    <v-card class="ma-10"> 
      <h3>Kreirajte novi senat</h3>
    </v-card>
    
  </div>

  <div>
    <form>
      <v-text-field class="unos"
        v-model = "name"
        :counter="10"
        label = "Ur.broj: "
        
      >
      </v-text-field>

      <v-text-field
        class="unos"
        label = "Unesite datum: "
        
      >
      </v-text-field>
    </form>

  </div>

  <!-- BUTTON ZA DODAVANJE NOVOG SENATA -->
  <div>
    <v-btn 
      id="plus"
      @click="kreiraj_novi_senat()" 
      icon="mdi-plus" size="small" >
    </v-btn>
  </div>
</template>


<script>
  export default {
    methods: {
      kreiraj_novi_senat(){
        window.open("/novi_senat", "_self")
      },

    }
  }
</script>


<style>
  .ma-10{
    text-align: center;
    background-color: skyblue;
    
    height: 50px;
    
  }
  
  .unos{
    width: 30%;
    margin-left: 20px;
    margin-top: 50px;
  }

  #plus{
    background-color:skyblue;
    margin-top: 15px;
    margin-left: 20px;
  }
  
</style>