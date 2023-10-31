<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Sidebar from './components/Sidebar.vue'
import Container from './components/Container.vue'

import ContentList from './components/ContentList.vue'
import CommentCard from './components/CommentCard.vue'
</script>

<template>
  <Header />
  <Sidebar />

  <Container>
    <ContentList>
      <CommentCard />
      <CommentCard />
      <CommentCard />
    </ContentList>
  </Container>

  <!-- <RouterView /> -->
</template>

<style scoped></style>
