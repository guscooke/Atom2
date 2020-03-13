<template>
  <v-content>
    <div class="staticHero">
      <v-row align="end" class="lightbox white--text pa-2 fill-height">
        <v-col>
          <v-container>
            <div class="headline">Entre em Contato</div>
          </v-container>
        </v-col>
      </v-row>
    </div>

    <div class="block">
      <v-container>
        <v-form ref="form" v-model="valid" lazy-validation>
          <v-text-field
            v-model="nome"
            :counter="10"
            :rules="nameRules"
            label="Name"
            required
          ></v-text-field>
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>
          <v-textarea
            v-model="mensagem"
            :rules="messageRules"
            label="Message"
            required
          ></v-textarea>
          <v-btn
            :disabled="!valid"
            color="success"
            class="mr-4"
            @click="validate"
            >Enviar</v-btn
          >
          <v-btn color="error" class="mr-4" @click="reset">Reset</v-btn>
        </v-form>
      </v-container>
    </div>

    <div class="googlemap">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3658.194268119185!2d-46.67931179999998!3d-23.525514200000007!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94cef807f7fb8f23%3A0xa6ebd7b5ff2dcd7c!2sComercial%20Casa%20das%20Caldeiras!5e0!3m2!1spt-BR!2sbr!4v1583980550984!5m2!1spt-BR!2sbr"
        width="100%"
        height="450"
      ></iframe>
    </div>
  </v-content>
</template>

<script>
export default {
  name: "Contact",
  data: () => ({
    valid: true,
    name: "",
    nameRules: [
      v => !!v || "Name is required",
      v => (v && v.length <= 10) || "Nome precisa ter no mínimo 10 caracteres"
    ],
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v => /.+@.+\..+/.test(v) || "E-mail preciso ser valido"
    ],
    message: "",
    messageRules: [
      v => !!v || "Message is required",
      v =>
        (v && v.length >= 10) || "Mensagem precisa ter no minimo 10 caracteres"
    ]
  }),

  methods: {
    validate() {
      if (this.$refs.form.validate()) {
        this.snackbar = true;
      }
    },
    reset() {
      this.$refs.form.reset();
    }
  }
};
</script>
