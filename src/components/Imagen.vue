<template>
  <div class="row">
    <div class="col-4"  v-for="item in items" :key="item.name">
      <v-card class="mx-auto" max-width="400">
        <v-img
          class="white--text align-end"
          height="200px"
          :src="item.image"
          contain
        >
        </v-img>

        <v-card-subtitle class="pb-0"> {{ item.name }} </v-card-subtitle>
      </v-card>
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        name: "Iconos de IoT",
        image: require("@/assets/Iconos de IoT.jpg"),
        profetion: "Software developer engineer",
        infomation: "Software developer",
      },
      {
        name: "Carlos Cohen",
        image: require("@/assets/ahorrar-agua.png"),
        profetion: "Software developer engineer and teacher Cecar",
        infomation: "Teacher Cecar",
      },
      {
        name: "Carlos Cohen",
        image: require("@/assets/ahorrar-agua.png"),
        profetion: "Software developer engineer and teacher Cecar",
        infomation: "Teacher Cecar",
      },
      {
        name: "Carlos Cohen",
        image: require("@/assets/ahorrar-agua.png"),
        profetion: "Software developer engineer and teacher Cecar",
        infomation: "Teacher Cecar",
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