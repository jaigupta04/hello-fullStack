<template>
  <v-app>

    <v-app-bar color="#0d1117" >

      <router-link to="/" class="mx-4">
        <img
          alt="Logo"
          src="@/assets/vue.svg"
          width="40"
          transition="scale-transition"
        />
      </router-link>

      <v-btn color="#57606a" rounded="xl" :exact="true" variant="flat" :ripple="false" class="ml-4" to="/">Home</v-btn>
      <v-btn color="#57606a" rounded="xl" :exact="true" variant="flat" :ripple="false" class="ml-4" to="/about">About</v-btn>

      <v-spacer></v-spacer>

    </v-app-bar>

    <v-main class="bg-app">
      <v-container fluid>
        <RouterView :doGet="doGet" :doPost="doPost" />
      </v-container>
    </v-main>

  </v-app>
</template>

<script>
import { RouterLink, RouterView } from 'vue-router'
import axios from "axios";

export default {

  data() {
    return {}
  },

  watch: {},

  mounted() {},

  methods: {}

};
</script>

<style scoped>

.bg-app {
  background-color: #57606a; 
}

</style>
