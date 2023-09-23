<template>
  <v-footer dark padless>
    <v-card class="flex" flat tile>
      <v-card-title class="cont">
        <strong class="subheading">contactame </strong>

        <v-spacer></v-spacer>

        <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
          <a href="https://www.linkedin.com/in/jeremiasbtorres/"
            ><v-icon size="24px">
              {{ icon }}
            </v-icon>
          </a>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        {{ new Date().getFullYear() }} — <strong>jeremias torres</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: ["mdi-linkedin"],
  }),
};
</script>

<style scoped>
.cont {
  background-color: rgb(29, 48, 66);
}
</style>
