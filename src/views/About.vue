<template>
  <v-content>
    <div class="staticHero">
      <v-img src="">
        <v-row align="end" class="lightbox white--text pa-2 fill-height">
          <v-col>
            <v-container>
              <div class="headline">About Us</div>
            </v-container>
          </v-col>
        </v-row>
      </v-img>
    </div>
    <div class="block">
      <v-container>
        <h2 class="text-center">Sobre Nós</h2>
        <p>
          Ea pri vitae antiopam theophrastus, ut sit erat putent eruditi. Qui at
          mutat adversarium. Postulant delicatissimi ei qui, an nonumy dolorem
          nam. Cu philosophia instructior pri, nec cu mutat homero saperet, cu
          paulo ridens legendos has. Cu veri oportere pri, ad integre numquam
          iudicabit mel. Nec ea ferri iudicabit dissentiet. Ex solet melius
          omittantur his, in gloriatur vulputate mel. Ad nostro repudiandae ius,
          est amet molestie te. No est modus sensibus volutpat, et putent
          dissentias has, et sea eirmod vivendum. Paulo lucilius expetenda sea
          in, cu nam mazim sanctus ponderum. Te nam mundi corpora, dicat dolore
          debitis ius in. Indoctum adversarium definitionem an pro, an eam vidit
          utinam detracto.
        </p>
      </v-container>
    </div>
    <v-parallax
      src="https://images.unsplash.com/photo-1547119957-637f8679db1e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1000&q=80"
    ></v-parallax>
    <Team />
  </v-content>
</template>

<script>
import Team from "../components/Team";

export default {
  name: "About",

  components: {
    Team
  }
};
</script>
