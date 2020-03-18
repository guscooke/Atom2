<template>
  <div class="the team">
    <v-container>
      <h2 class="text-center">Quem Somos!</h2>
      <v-row>
        <v-col v-for="item in items" :key="item.id" cols="12" md="6">
          <v-card outlined class="mx-auto">
            <v-img
              class="white--text align-center"
              height="200px"
              :src="item.src"
            >
              <v-avatar class="profile" color="grey" size="156" title>
                <v-img src="item.src"></v-img>
              </v-avatar>
              <v-card-title>{{ item.title }}</v-card-title>
            </v-img>
            <v-card-subtitle class="pb-0">{{ item.subtitle }}</v-card-subtitle>
            <v-card-actions>
              <v-btn color="purple" text>
                Resume
              </v-btn>

              <v-spacer></v-spacer>

              <v-btn icon @click="show = !show">
                <v-icon>{{
                  show ? "mdi-chevron-up" : "mdi-chevron-down"
                }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  {{ item.description }}
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "Team",
  data: () => ({
    show: false,
    items: [
      {
        id: 1,
        title: "Founder CTO",
        subtitle: "Daniel Cassiano",
        description:
          "IT Executive with about 17 years of experience inside large organizations and startups. I am focussed on leading teams merging technical, product and business visions through the right way, building both strategic, management and technical sides. My main challenge right now is to lead the Digital Technology of Magalu and organization's transformation into a Data-Driven one, democratizing data, science, tools, and mostly: the ability to make decisions even inside large scale products or a common sales analysis with the power of Machine Learning and IA, in the most simple way we can. I am a specialist on scaling teams (people, processes and technology) inside both chaordic and boostraping organizationsI led teams in a lot of areas inside IT ecosystem: web platforms, mobile products, infrastructure, cybersecurity, financial, but my main field of expertise is with Data (Engineering, Science, ML, IA), specially building Data Products.Speaking of my technical side, I have solid experience with software architecture and engineering (mostly backend but also front-end), APIs, big data processing (since 2009), search platforms, sort and ranking algorithms, also location-based systems.I worked with a lot of technologies, frameworks and programming languages on my entire career even coding or leading teams and projects, so I'm agnostic with them and my goal is to choose the right tool to solve the problem besides my personal preferences.  ",
        src: require("../assets/images/img10.jpg"),
        
      },
      {
        id: 2,
        title: "Founder",
        subtitle: "Gustavo Cooke",
        description:
          "All starts with Brokerage firms over the nineties as an intern to finally become a Stock Broker, three firms laters I tried different sectors such as telecom sector, chemical Trading Company , BiofueIs and Commodities, spent most of my years as sales, trader and broker.I also dedicated a great number of years building a strong network with major participants in the Biofuel and Sugar industries from Mills, Bio-Refineries, Trading Companies, Marketers and Distributors.Entrepreneurism called me several times, I have ventured my own businesses over the past 8 years and I still do.",
        src: require("../assets/images/img15.jpg")
      }
    ]
  })
};
</script>
