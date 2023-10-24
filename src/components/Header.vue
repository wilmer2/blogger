<script setup lang="ts">
import Search from './Search.vue'
import Avatar from './Avatar.vue'
</script>

<template>
  <header>
    <div class="header-menu">
      <div>
        <span class="material-symbols-outlined letter-icon"> menu </span>
      </div>
      <figure class="ml-1">
        <img class="header-logo" src="@/assets/images/logo_blogger.png" alt="Blogger logo" />
      </figure>
    </div>

    <div class="header-interactive-container">
      <Search />
      <Avatar />
    </div>
  </header>
</template>

<style scoped>
header {
  position: relative;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  padding-left: 12px;
  padding-right: 12px;
}

.header-menu {
  display: flex;
  align-items: center;
}

.header-logo {
  width: 40px;
  height: 40px;
}

.header-interactive-container {
  display: flex;
  justify-content: flex-end;
  flex: 1;
}

figure {
  display: none;
}

@media (width >= 600px) {
  figure {
    display: block;
    margin-right: 16px;
  }
}
</style>
