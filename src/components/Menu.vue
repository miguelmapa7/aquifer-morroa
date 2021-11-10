<template>
  <v-card id="card">
    <v-navigation-drawer v-model="drawer" :mini-variant.sync="mini" permanent>
      <v-list-item class="px-2">
        <v-list-item-avatar>
          <v-img src="../assets/ahorrar-agua.png"></v-img>
        </v-list-item-avatar>

        <v-list-item-title>Menú</v-list-item-title>

        <v-btn icon @click.stop="mini = !mini">
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          v-on:click.stop="item.methods"
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
  data() {
    return {
      drawer: true,
      items: [
        {
          title: "Inicio",
          icon: "mdi-home-city",
          methods: () => this.login(),
        },
        {
          title: "Nosotros",
          icon: "mdi-account",
          methods: () => this.about(),
        },
        {
          title: "Investigación",
          icon: "mdi-animation",
          methods: () => this.investigacion(),
        },
        {
          title: "Desarrollo",
          icon: "mdi-apple-keyboard-command",
          methods: () => this.desarrollo(),
        },
        {
          title: "Productos",
          icon: "mdi-application-braces-outline",
          methods: () => this.productos(),
        },
        {
          title: "Descargas",
          icon: "mdi-arrow-down-bold-hexagon-outline",
          methods: () => this.descargas(),
        },
        {
          title: "Aportes",
          icon: "mdi-arrow-decision-auto",
          methods: () => this.aportes(),
        },
        {
          title: "Imágenes",
          icon: "mdi-alpha-i-box-outline",
          methods: () => this.imagenes(),
        },
        {
          title: "Bibliografía y Manuales",
          icon: "mdi-file-table-box-multiple",
          methods: () => this.manuales(),
        },
        {
          title: "Contacto",
          icon: "mdi-card-account-details-star",
          methods: () => this.contacto(),
        },
      ],
      mini: true,
    };
  },
  methods: {
    login() {
      console.log("Inicio");
      this.$router.push("/inicio").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    about() {
      console.log("Nosotros");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    investigacion() {
      console.log("Investigación");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    desarrollo() {
      console.log("Desarrollo");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    productos() {
      console.log("Productos");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    descargas() {
      console.log("Descargas");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    aportes() {
      console.log("Aportes");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    imagenes() {
      console.log("Imagenes");
      this.$router.push("/imagen").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    manuales() {
      console.log("Manuales");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
    contacto() {
      console.log("Contacto");
      this.$router.push("/about").catch((error) => {
        if (error.name != "NavigationDuplicated") {
          throw error;
        }
      });
    },
  },
};
</script>

<style>
#card {
  margin-top: 30pt;
  margin-bottom: 10pt;
}
</style>