<script setup lang="ts">
import Search from './Search.vue'
import Avatar from './Avatar.vue'
</script>

<template>
  <header>
    <div class="header-menu-container">
      <div class="header-menu">
        <div>
          <span class="material-symbols-outlined letter-icon"> menu </span>
        </div>
        <figure class="ml-1">
          <img class="header-logo" src="@/assets/images/logo_blogger.png" alt="Blogger logo" />
        </figure>
      </div>
      <Search />
    </div>

    <div class="header-interactive-container">
      <Avatar />
    </div>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;
  padding-top: 10px;
  padding-left: 12px;
  padding-right: 12px;
}

.header-menu-container {
  position: relative;

  display: flex;
  justify-content: space-between;
  flex: 1;
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

@media (width >= 720px) {
  header {
    padding-left: 16px;
    padding-right: 16px;
  }
}
</style>
