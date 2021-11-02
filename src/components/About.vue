<template>
<div class="row" id="cards" >
    <div class="col-4" 
    v-for="item in items" 
    :key="item.name" >
  
      <v-card class="mx-auto" max-width="344" id="card">
        <v-img
          :src= "item.image"
          height="300"
          class="grey darken-4"
        ></v-img>

        <v-card-title> {{item.name}}</v-card-title> 

        <v-card-subtitle> {{item.profetion}} </v-card-subtitle>

        <v-card-actions>
          <v-btn color="orange lighten-2" text> About Him </v-btn>

          <v-spacer></v-spacer>

          <v-btn icon @click="show = !show">
            <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show">
            <v-divider></v-divider>

            <v-card-text> {{item.infomation}} </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
    
  </div>
   </div>
</template>

<script>
export default {
  data: () => ({
    show: false,
    items: [
      {
        name: "Miguel Andrés Pérez Arcia",
        image: require("@/assets/FotoPerfil.jpeg"),
        profetion: "Software developer engineer",
        infomation: "Software developer",
      },
      {
        name: "Carlos Cohen",
        image: require("@/assets/ahorrar-agua.png"),
        profetion: "Software developer engineer and teacher Cecar",
        infomation: "Teacher Cecar",
      },
    ],
  }),
};
</script>

<style>
</style>