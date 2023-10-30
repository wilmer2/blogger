<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import Container from './components/Container.vue'
import CommentCard from './components/CommentCard.vue'
</script>

<template>
  <Header />
  <!-- <Sidebar /> -->

  <Container>
    <CommentCard />
  </Container>

  <!-- <RouterView /> -->
</template>

<style scoped></style>
