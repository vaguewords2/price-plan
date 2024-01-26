<script setup>
import Plan from './Plan.vue'
</script>
<template>
  <v-layout class="rounded rounded-md">
    <v-app-bar>
      <v-container><v-img :width="32" src="/img/logo/symbol.svg"></v-img></v-container>
    </v-app-bar>
    <v-main style="min-height: 100vh;">
      <Plan />
    </v-main>
  </v-layout>
</template>
<script>
export default {
  name: 'Layout'
}
</script>