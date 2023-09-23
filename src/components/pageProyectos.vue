<template>
  <v-container>
    <v-card class="elevation-5 cont py-4 px-2">
      <v-card-title class="text-h4 orange lighten-1 mb-4 white--text"
        >Proyectos</v-card-title
      >
      <v-row>
        <v-col
          cols="12"
          sm="6"
          md="4"
          lg="3"
          v-for="project in projects"
          :key="project.name"
        >
          <div>
            <v-card class="mb-4 cont white--text">
              <v-img
                :src="require('@/assets/' + project.image)"
                height="200"
              ></v-img>
              <v-card-title>{{ project.name }}</v-card-title>
              <v-card-text class="white--text">{{
                project.description
              }}</v-card-text>
              <v-card-actions>
                <v-btn
                  color="orange lighten-1"
                  text
                  @click="verProyecto(project.url)"
                  >Ver proyecto</v-btn
                >
              </v-card-actions>
            </v-card>
          </div>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "DigitalWebCraft",
          description:
            "Una página para publicitar mi negocio de creación de páginas web",
          image: "proyecto1.png",
          url: "https://jeremias-t.github.io/DigitalWebCraft/",
        },
        
      ],
    };
  },
  methods: {
    verProyecto(url) {
      window.open(url, "_blank");
    },
  },
};
</script>

<style scoped>
.cont {
  background-color: rgb(29, 48, 66);
  margin-bottom: 2rem;
}
</style>
