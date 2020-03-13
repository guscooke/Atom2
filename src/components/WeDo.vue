<template>
  <div class="block latestPostBlock">
    <transition :duration="{ enter: 300, leave: 500 }"> </transition>
    <v-container>
      <h2 class="text-center">Serviços</h2>

      <v-row>
        <v-col v-for="item in items" :key="item.id" cols="12" md="4">
          <v-card outlined class="mx-auto">
            <v-img class="white--text align-end" height="300px" :src="item.src">
              <v-card-title>{{ item.title }}</v-card-title>
            </v-img>
            <v-card-subtitle class="pb-0">{{ item.subtitle }}</v-card-subtitle>
            <v-card-text class="text--primary">
              <div>{{ item.description }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn color="primary" text></v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Block",
  data: () => ({
    show: false,
    items: [
      {
        id: 1,
        title: "Web App",
        subtitle: "Software sob Medida",
        description:
          "Capacitamos nossos clientes com aplicativos Web adaptáveis, usando tecnologias e práticas Web de código aberto e proprietárias para simplificar fluxos de trabalhos complexos.",
        src: require("../assets/images/img3.jpg")
      },
      {
        id: 2,
        title: "Mobile App",
        subtitle: "IOS, Android e Windows Phone e Hibrido",
        description:
          "Nossos serviços capacitam as organizações com aplicativos móveis para android, ios e windows. Seja multiplataforma, nativa ou híbrida, garantimos uma entrega eficiente e econômica.",
        src: require("../assets/images/img32.jpg")
      },
      {
        id: 3,
        title: "Insights",
        subtitle: "Ciência de Dados",
        description:
          "Nossos serviços de análise e vizualização de dados ajudam as organizações a explorar novos recursos, otimizar processos existentes, aprimorar as habilidades de previsão e responder melhor às mudanças do mercado.",
        src: require("../assets/images/img5.jpg")
      }
    ]
  })
};
</script>
