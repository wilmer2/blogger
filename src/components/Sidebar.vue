<script setup lang="ts">
import { RouterLink } from 'vue-router'
import SidebarButton from './SidebarButton.vue'
import Select from './Select.vue'
</script>
<template>
  <figure>
    <img class="logo" src="@/assets/images/logo_blogger.png" alt="Logo" />
  </figure>
  <div><Select /></div>
  <div>
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
</template>

<style scoped>
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
</style>
