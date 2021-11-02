<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="./assets/ahorrar-agua.png"
          transition="scale-transition"
          width="60"
        />

        <div class="d-flex align-center">
          <p class="font-weight-black" id="title">Acuefero de Morroa</p>
        </div>
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>
    <br />
    <div id="contenedorTodo">
      <div id="contenedorUno">
        <Menu />
      </div>
      <div id="contenedorDos">
        <v-main>
          <router-view />
        </v-main>
      </div>
    </div>
    <br />
    <Footer />
  </v-app>
</template>

<script>
import Footer from "./components/Footer.vue";
import Menu from "./components/Menu.vue";

export default {
  name: "App",

  data: () => ({
    //
  }),
  components: {
    Footer,
    Menu,
  },
};
</script>
<style>
#title {
  font-size: 30px;
  margin-top: 15px;
}
#contenedorTodo {
  width: 100%;  
  display:flex;
}
#contenedorDos {
  width: 90%; 
  margin-left: 30px; 
}
</style>