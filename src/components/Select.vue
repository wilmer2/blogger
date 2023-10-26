<script setup lang="ts">
import { ref, type Ref } from 'vue'

const showMenu: Ref<boolean> = ref(false)

const handleShowMenu = (): void => {
  showMenu.value = true
}
</script>
<template>
  <div class="main-container">
    <div class="title-container" @click="handleShowMenu">
      <div><span>My Blog</span></div>
      <div><span class="material-symbols-outlined arrow-icon"> arrow_drop_down </span></div>
    </div>
    <div class="options-container" v-if="showMenu">
      <div class="options-label">Tus blogs</div>
      <div class="options-list">
        <div class="options-item">My Blog</div>
        <div class="options-item">Second Blog</div>
      </div>
      <div class="options-action-container">
        <div class="options-item">Nuevo blog...</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  position: relative;
}

.options-container {
  position: absolute;
  top: 0;
  width: 100%;
  background-color: white;
  box-shadow: 1px 1px 6px -1px rgba(168, 171, 172, 0.75);
  z-index: 999999;
}
.title-container {
  display: flex;
  justify-content: space-between;
  cursor: pointer;
}

.arrow-icon {
  color: var(--gray-ligth-color);
}
.options-label {
  padding: 12px;
  color: #b8b8bd;
}

.options-list {
  padding-bottom: 8px;
  margin-bottom: 8px;
  border-bottom: 1px solid var(--border-color);
}

.options-item {
  padding: 15px 12px 15px 15px;
  cursor: pointer;
}

.options-item:hover {
  background-color: #eeeeee;
}
</style>
