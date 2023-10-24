<script setup lang="ts">
import { ref, type Ref, onMounted } from 'vue'

const visibleInput: Ref<boolean> = ref(false)
const textInput: Ref<string> = ref('')
const responsive = window.matchMedia('(min-width: 600px)')

const changeSizeScreen = (): void => {
  if (responsive.matches) {
    visibleInput.value = true
  } else {
    visibleInput.value = false
  }
}

const handleShowInput = (): void => {
  visibleInput.value = true
}

const handleHideInput = (): void => {
  visibleInput.value = false
  textInput.value = ''
}

responsive.addEventListener('change', changeSizeScreen)

onMounted(() => {
  changeSizeScreen()
})
</script>

<template>
  <div class="search-container-btn" v-if="!visibleInput" @click="handleShowInput">
    <span class="material-symbols-outlined letter-icon"> search </span>
  </div>

  <div class="input-container" v-else="visibleInput">
    <div class="input-arrow-container">
      <span class="material-symbols-outlined letter-icon search-input"> search </span>

      <span class="material-symbols-outlined letter-icon arrow-input" @click="handleHideInput">
        arrow_back
      </span>
      <input class="ml-1" type="text" placeholder="Buscar entradas" v-model="textInput" />
    </div>
    <span class="material-symbols-outlined letter-icon"> info </span>
  </div>
</template>

<style scoped>
.input-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-left: 12px;
  padding-right: 12px;
  width: 100%;
  height: 48px;
  margin-left: 16px;
  max-width: 720px;
  border-radius: 12px;
  background-color: white;
  box-shadow: 1px 1px 5px 0px rgba(168, 171, 172, 1);
  z-index: 1000;
}

.input-arrow-container {
  display: flex;
}

.search-container-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 45px;
  height: 48px;
  border-radius: 8px;
  box-sizing: border-box;

  background: var(--bg-primary);
}

input {
  height: 100%;
  background-color: transparent;
  border: 1px solid transparent;
  font-size: var(--font-medium);
}

input::placeholder {
  color: var(--gray-color);
  font-family: Roboto, sans-serif;
  font-weight: 400;
  opacity: 0.6;
}

@media (width >= 600px) {
  .input-container {
    margin: 0 auto;
    background-color: var(--bg-primary);
  }

  .arrow-input {
    display: none;
  }

  .search-input {
    display: block;
  }
}
</style>
