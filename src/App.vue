<template>
  <v-app>
    <v-app-bar app color="" dark>
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
          <p class="font-weight-black" id="title">
            Repositorio del proyecto IHMoGA
          </p>
        </div>
      </div>
    </v-app-bar>
    <br />
    <div class="col" >
      <div class="d-flex align-center" id="sub-title" >
        <p class="font-weight-black">
          Implementación de herramientas de monitoreo para la gestión de
          acuíferos en el departamento de Sucre a través del Internet de las
          Cosas de Nueva Generación
        </p>
      </div>

      <div id="contenedorTodo" >
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
    </div>
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
#sub-title {
  font-size: 18px;
  margin-top: 45px;
  margin-left: 50px;
  margin-right: 90px;
  /*background-color: aliceblue;*/
}
#contenedorTodo {
  width: 100%;
  display: flex;
  /*background-color: aqua;*/
}
#contenedorDos {
  width: 90%;
  margin-left: 30px;
  /*background-color: rgb(115, 255, 0);*/
  margin-bottom: 10px;
  margin-top: 1px;
}
#contenedorUno {
  /*background-color: rgb(255, 174, 0);*/
  margin-left: 5px;
}
</style>