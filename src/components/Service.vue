<template>
  <div class="block">
    <v-container>
      <h2 class="text-center">Transforme suas Ideias</h2>
      <p class="text-center">
        O parceiro de desenvolvimento de software certo pode mudar tudo!
        Ajudamos as empresas de tecnologia a ampliar, fornecendo soluções ágeis
        de desenvolvimento de software
      </p>
      <v-row>
        <v-col
          v-for="item in items"
          :key="item.id"
          class="d-flex child-flex"
          cols="12"
          sm="4"
        >
          <v-card flat tile class="mx-auto">
            <v-img
              :src="item.src"
              aspect-ratio="1"
              class="grey lighten-2"
            ></v-img>
            <v-card-text class="text--primary text-center">
              <div class="title">{{ item.name }}</div>
              <p>{{ item.title }}</p>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      items: [
        {
          id: 1,
          src: require("../assets/images/atom1.png"),
          name: "",
          title: "Consultoria"
        },
        {
          id: 2,
          src: require("../assets/images/atom2.png"),
          name: "",
          title: "Software lab"
        },
        {
          id: 3,
          src: require("../assets/images/atom3.png"),
          name: "",
          title: "Saas"
        }
      ]
    };
  }
};
</script>