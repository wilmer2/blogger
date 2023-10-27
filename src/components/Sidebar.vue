<script setup lang="ts">
import { RouterLink } from 'vue-router'
import SidebarButton from './SidebarButton.vue'
import Select from './Select.vue'
</script>
<template>
  <div class="sidebar-container">
    <figure>
      <img class="logo" src="@/assets/images/logo_blogger.png" alt="Logo" />
    </figure>
    <div class="select-container"><Select /></div>
    <div class="button-container">
      <SidebarButton />
    </div>
    <ul>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> article </span>
          <span>Entradas</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> stacked_bar_chart </span>
          <span>Estadísticas</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> mode_comment </span>
          <span>Comentarios</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> attach_money </span>
          <span>Ingresos</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> filter_none </span>
          <span>Páginas</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> wysiwyg </span>
          <span>Diseño</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> imagesearch_roller </span>
          <span>Tema</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> settings </span>
          <span>Configuración</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> bookmark </span>
          <span>Lista de Lectura</span>
        </RouterLink>
      </li>
      <li>
        <RouterLink class="link" to="/">
          <span class="material-symbols-outlined list-icon"> open_in_new </span>
          <span> Ver el blog </span>
        </RouterLink>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.sidebar-container {
  position: fixed;
  top: 0;
  width: 264px;
  height: 100%;
  max-height: 100vh;
  overflow-y: auto;
  background-color: white;
  box-shadow: 1px 1px 6px -1px rgba(168, 171, 172, 0.75);
  z-index: 2000;
}

.button-container {
  width: 220px;
  margin-bottom: 10px;
  padding-left: 16px;
  padding-bottom: 20px;
  border-bottom: 1px solid var(--border-color);
}

.select-container {
  padding-left: 16px;
  max-width: 240px;
  margin-bottom: 20px;
}

.logo {
  width: 40px;
  height: 40px;
}
.list-icon {
  margin-right: 16px;
  color: #546e7a;
}

.link {
  display: flex;
  align-items: center;
  padding: 12px 0 12px 32px;
}

figure {
  padding-top: 12px;
  padding-left: 16px;
  margin-bottom: 30px;
}

@media (width >= 1024px) {
  figure {
    display: none;
  }

  .sidebar-container {
    top: 70px;
    width: 280px;
    border-right: 1px solid var(--border-color);
    max-height: calc(100vh - 80px);
    box-shadow: 0 0;
  }

  .select-container {
    padding-top: 20px;
  }
}
</style>
