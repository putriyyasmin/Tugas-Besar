<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import LeftNav from './components/navbar/LeftNav.vue'
</script>


<template>
  <v-app style="margin-left: -50px;">
    <LeftNav />
    <v-main style="width: 100dvw;">
      <router-view />
    </v-main>
  </v-app>
</template>
