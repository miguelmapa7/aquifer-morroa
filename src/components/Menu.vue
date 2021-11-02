<template>
  <v-card id="card">
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant.sync="mini"
      permanent
    >
      <v-list-item class="px-2">
        <v-list-item-avatar>
          <v-img src="../assets/ahorrar-agua.png"></v-img>
        </v-list-item-avatar>

        <v-list-item-title>Menú</v-list-item-title>

        <v-btn
          icon
          @click.stop="mini = !mini"
        >
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          @click="item.method"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
            
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        drawer: true,
        items: [
          { title: 'Inicio', icon: 'mdi-home-city' , method: () => this.login()},
          { title: 'Nosotros', icon: 'mdi-account', method: () => this.about()},
          { title: 'Investigación', icon: 'mdi-animation' },
          { title: 'Desarrollo', icon: 'mdi-apple-keyboard-command' },
          { title: 'Productos', icon: 'mdi-application-braces-outline' },
          { title: 'Descargas', icon: 'mdi-arrow-down-bold-hexagon-outline' },
          { title: 'Aportes', icon: 'mdi-arrow-decision-auto' },
          { title: 'Imágenes', icon: 'mdi-alpha-i-box-outline' },
          { title: 'Bibliografía y Manuales', icon: 'mdi-file-table-box-multiple' },
          { title: 'Contacto', icon: 'mdi-card-account-details-star' },
        ],
        mini: true,
      }
    },
    methods: {
        login(){
            console.log('Prueba')
            this.$router.push('/inicio')
        },
        about(){
            console.log('About')
            this.$router.push('/about')
        },
    }
  }
</script>

<style>
#card{
    margin-top: 50pt;
}
</style>