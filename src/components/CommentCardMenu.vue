<script setup lang="ts">
import { ref, type Ref } from 'vue'

const showMenu: Ref<boolean> = ref(false)
const responsive = window.matchMedia('(min-width: 768px)')

const handleHideMenu = (): void => {
  showMenu.value = false
}

const handleShowMenu = (): void => {
  showMenu.value = true
}

responsive.addEventListener('change', handleHideMenu)
</script>

<template>
  <div class="p-relative">
    <div class="menu-icon-container">
      <span class="material-symbols-outlined letter-icon" @click="handleShowMenu"> more_vert </span>
      <div class="menu-options" v-if="showMenu">
        <ul>
          <li>
            <div class="mr-1">
              <span class="material-symbols-outlined letter-icon"> dangerous </span>
            </div>
            <div class="list-text-container">
              <span> Quitar contenido </span>
            </div>
          </li>
          <li>
            <div class="mr-1">
              <span class="material-symbols-outlined letter-icon"> report </span>
            </div>
            <div class="list-text-container">
              <span>Spam</span>
            </div>
          </li>
          <li>
            <div class="mr-1">
              <span class="material-symbols-outlined letter-icon"> delete </span>
            </div>
            <div class="list-text-container">
              <span>Borrar</span>
            </div>
          </li>
        </ul>
      </div>
    </div>

    <div class="option-icon-container">
      <div class="option-icon">
        <span class="material-symbols-outlined letter-icon"> dangerous </span>
      </div>
      <div class="option-icon">
        <span class="material-symbols-outlined letter-icon"> report </span>
      </div>
      <div class="option-icon">
        <span class="material-symbols-outlined letter-icon"> delete </span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.letter-icon {
  color: #444444;
}

.option-icon-container {
  position: absolute;
  top: 3px;
  left: -164px;
  display: none;
}

.option-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  margin-left: 16px;
  color: #37474f;
  border-radius: 50%;
}

.option-icon:hover {
  background-color: #eceff1;
}

ul {
  position: absolute;
  top: 24px;
  left: -202px;
  padding-top: 8px;
  padding-bottom: 15px;
  width: 220px;
  background-color: white;
  border: 1px solid var(--border-color);
  box-shadow: var(--card-shadow);
  z-index: 999;
}

li {
  display: flex;
  align-items: center;
  padding: 10px 0 10px 16px;
  color: #37474f;
  font-size: 16px;
}

li:hover {
  background: var(--bg-primary);
}
.list-text-container {
  padding-bottom: 4px;
}

@media (width >= 768px) {
  .menu-icon-container {
    display: none;
  }
}
</style>
