<template>
  <v-app id="inspire">
    <navbar></navbar>

    <v-main>
      <index></index>
    </v-main>
  </v-app>
</template>

<script setup>
import { ref } from "vue";
import navbar from "./components/navbar.vue";
import index from "./components/index.vue";
</script>
