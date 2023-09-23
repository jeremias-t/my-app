<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app dark color="blue-grey darken-2">
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="orange lighten-1--text text--accent-4"
        >
          <v-list-item>
            <v-list-item-title>
              <a class="link" href="#inicio"> Inicio</a></v-list-item-title
            >
          </v-list-item>

          <v-list-item>
            <v-list-item-title
              ><a class="link" href="#mi">Sobre mi</a></v-list-item-title
            >
          </v-list-item>

          <v-list-item>
            <v-list-item-title
              ><a class="link" href="#skill">Skills</a></v-list-item-title
            >
          </v-list-item>

          <v-list-item>
            <v-list-item-title
              ><a class="link" href="#proyecto">proyectos</a></v-list-item-title
            >
          </v-list-item>

          <v-list-item>
            <v-list-item-title
              ><a class="link" href="#contacto">contacto</a></v-list-item-title
            >
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app dark color="blue-grey darken-2">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="white--text">Jeremías</v-toolbar-title>
    </v-app-bar>

    <v-main class="main">
      <page-inicio id="inicio" />
      <page-mi id="mi" />
      <page-skill id="skill" />
      <page-proyectos id="proyecto" />
      <page-contacto id="contacto" />
      <page-footer />

      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import PageContacto from "./components/pageContacto.vue";
import PageFooter from "./components/pageFooter.vue";
import pageInicio from "./components/pageInicio.vue";
import PageMi from "./components/pageMi.vue";
import PageProyectos from "./components/pageProyectos.vue";
import PageSkill from "./components/pageSkill.vue";

export default {
  components: {
    pageInicio,
    PageMi,
    PageSkill,
    PageProyectos,
    PageContacto,
    PageFooter,
  },
  data: () => ({
    drawer: false,
    menuItems: [
      { title: "Inicio", route: "/inicio" },
      { title: "Sobre mí", route: "/sobre-mi" },
      { title: "Skills", route: "/skills" },
      { title: "Proyectos", route: "/proyectos" },
      { title: "Contacto", route: "/my-app/src/components/pageContacto.vue" },
    ],
  }),
  methods: {
    navigateTo(route) {
      this.$router.push(route);
      this.drawer = false;
    },
  },
};
</script>

<style scoped>
.main {
  background-color: rgb(22, 38, 53);
}
.link {
  text-decoration: none;
  color: white;
  font-size: 1.2rem;
}
</style>
