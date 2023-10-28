<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import Container from './components/Container.vue'
import Card from './components/Card.vue'
</script>

<template>
  <Header />
  <!-- <Sidebar /> -->

  <Container>
    <Card />
    <Card />
  </Container>

  <!-- <RouterView /> -->
</template>

<style scoped></style>
