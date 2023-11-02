<script setup lang="ts">
import { ref, type Ref } from 'vue'

const showMenu: Ref<boolean> = ref(false)

const handleShowMenu = (): void => {
  showMenu.value = true
}
</script>

<template>
  <div class="p-relative">
    <div class="menu-container" @click="handleShowMenu">
      <div class="menu-icon-container eye">
        <span class="material-symbols-outlined"> visibility </span>
        <span class="letter-color">Vista previa</span>
      </div>
      <div class="menu-icon-container arrow">
        <span class="material-symbols-outlined"> arrow_drop_down </span>
      </div>
    </div>

    <ul v-if="showMenu">
      <li>
        <span class="material-symbols-outlined"> visibility </span>
        <span class="list-text">Obtener vista previa de la entrada</span>
      </li>
      <li>
        <span class="material-symbols-outlined"> save </span>
        <span class="list-text">Guardar</span>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.menu-container {
  display: flex;
  align-items: center;
  border: 1px solid var(--border-color);
  border-radius: 2px;
  cursor: pointer;
}

.menu-icon-container {
  display: flex;
  align-items: center;
  padding: 8px 6px;
  color: rgba(0, 0, 0, 0.87);
  font-size: 500;
}

.menu-icon-container.arrow {
  padding-left: 4px;
  padding-right: 4px;
  border-left: 0.5px solid var(--border-color);
}

.letter-color {
  display: none;
  color: rgba(0, 0, 0, 0.87);
  font-size: 14px;
  font-weight: 500;
}

ul {
  position: absolute;
  left: -174px;
  width: 300px;
  border: 1px solid var(--border-color);
  background-color: white;
  box-shadow: var(--card-shadow);
  z-index: 999;
}

li {
  display: flex;
  align-items: center;
  padding: 10px;
  color: #37474f;
  font-size: 14px;
}

.list-text {
  margin-left: 8px;
}

@media (width > 840px) {
  ul {
    left: -33px;
  }
  .letter-color {
    display: inline-block;
    margin-left: 5px;
    padding-bottom: 1px;
  }
}
</style>
