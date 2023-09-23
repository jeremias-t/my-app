<template>
  <v-container class="">
    <v-card
      class="elevation-5 cont pa-4 d-flex flex-column justify-center align-center mt-4 mb-4"
    >
      <v-card-title class="text-h4 titulo">Sobre Mí</v-card-title>
      <v-card-text class="white--text text-h6">
        Hola, soy Jeremías, un entusiasta del desarrollo web con experiencia en
        diversos lenguajes y herramientas. Mi pasión por aprender nuevas
        tecnologías me impulsa constantemente. Disfruto equilibrar funcionalidad
        y diseño para crear experiencias web atractivas. Estoy dispuesto a
        enfrentar desafíos y trabajar en equipo para crear soluciones
        innovadoras. Mi objetivo es seguir creciendo en esta emocionante
        industria.
      </v-card-text>
      <v-card-actions>
        <v-btn icon @click="abrirLinkedIn">
          <v-icon>mdi-linkedin</v-icon>
        </v-btn>
        <v-btn icon @click="abrirGitHub">
          <v-icon>mdi-github</v-icon>
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
</template>

<script>
export default {
  methods: {
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
}

.titulo {
  color: #ffa726;
  font-weight: 700;
}
</style>
