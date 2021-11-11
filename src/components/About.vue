<template>
  <div class="row" id="cards">
    <div class="col-4" v-for="item in items" :key="item.name">
      <v-card class="mx-auto" max-width="300" id="card">
        <v-img :src="item.image" contain max-height="250" class="write write-4"></v-img>

        <v-card-title> {{ item.name }}</v-card-title>

        <v-card-subtitle> {{ item.profetion }} </v-card-subtitle>

        <v-card-actions>
          <v-btn color="orange lighten-2" text> Información </v-btn>

          <v-spacer></v-spacer>

          <v-btn icon @click="show = !show">
            <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show" style="margin-left: 10px;">
            <v-divider></v-divider>
            <v-card-text> {{ item.infomation }} </v-card-text>
            <div class="row" style=" margin: 2px;">
              
              <div class="" style=" padding: 4%; ">
                <v-icon>{{ item.icon }}</v-icon>
              </div>
              <div class="" >
                <v-card-text> {{ item.email }} </v-card-text>
              </div>
            </div>

            <v-divider></v-divider>
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
        name: "Carlos Cohen",
        image: require("@/assets/carlos-cohen.png"),
        profetion: "Software developer engineer and teacher Cecar",
        infomation:
          "MAGÍSTER INGENIERÍA DE SISTEMAS Y COMPUTACIÓN, PHD (C) PROYECTOS DE INGENIERÍA BASADOS EN TICS",
        icon: "mdi-email",
        email: "carlos.cohen@cecar.edu.co",
      },
      {
        name: "Miguel Andrés Pérez Arcia",
        image: require("@/assets/FotoPerfil.jpeg"),
        profetion: "Software developer engineer",
        infomation: "Software developer",
        icon: "mdi-email",
        email: "miguel.perezar@cecar.edu.co",
      },
    ],
  }),
};
</script>

<style>
</style>