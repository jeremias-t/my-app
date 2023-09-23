<template>
  <v-container>
    <v-card class="elevation-5 cont py-4 px-2">
      <v-card-title class="text-h4 orange lighten-1 mb-4 white--text"
        >Habilidades</v-card-title
      >
      <v-card-text>
        <v-row justify="center">
          <v-col
            cols="12"
            sm="6"
            md="4"
            lg="3"
            v-for="(skill, index) in skills"
            :key="index"
          >
            <v-chip class="ma-2 text-h6 orange lighten-1 white--text" outlined>
              {{ skill }}
            </v-chip>
          </v-col>
        </v-row>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        "HTML",
        "CSS",
        "Sass",
        "JavaScript",
        "Bootstrap",
        "Python",
        "Vue.js",
        "Vuetify",
        "Figma",
      ],
    };
  },
};
</script>

<style scoped>
.cont {
  background-color: #1d3042;
  margin-bottom: 2rem;
}
</style>
