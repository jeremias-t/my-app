<template>
  <v-container>
    <v-card class="elevation-5 cont pa-4">
      <v-card-title class="text-h4 orange lighten-1 mb-16 white--text"
        >Contáctame</v-card-title
      >
      <v-card-text class="white--text">
        ¿Tienes alguna pregunta o quieres trabajar en un proyecto juntos? ¡No
        dudes en contactarme!
      </v-card-text>
      <v-card-actions>
        <v-btn color="orange lighten-1" text @click="enviarCorreo"
          >Enviar Correo</v-btn
        >
        <v-btn icon @click="abrirLinkedIn">
          <v-icon class="orange--text">mdi-linkedin</v-icon>
        </v-btn>
        <v-btn icon @click="abrirGitHub">
          <v-icon class="orange--text">mdi-github</v-icon>
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
export default {
  methods: {
    enviarCorreo() {
      window.location.href = "mailto:portafoliotorer830@gmail.com";
    },
    abrirLinkedIn() {
      window.open("https://www.linkedin.com/in/jeremiasbtorres/", "_blank");
    },
    abrirGitHub() {
      window.open("https://github.com/jeremias-t", "_blank");
    },
  },
};
</script>

<style scoped>
.cont {
  background-color: rgb(29, 48, 66);
  margin-bottom: 4rem;
}
</style>
