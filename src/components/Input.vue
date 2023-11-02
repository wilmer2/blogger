<script setup lang="ts">
import { ref, type Ref } from 'vue'

const text: Ref<string> = ref('')
const activeLabel: Ref<boolean> = ref(false)

const handleDeactiveLabel = (): void => {
  if (!text.value) {
    activeLabel.value = false
  }
}

const handleActiveLabel = (): void => {
  activeLabel.value = true
}
</script>
<template>
  <div class="p-relative mt-2">
    <div class="input-container">
      <input
        type="text"
        class="input"
        v-model="text"
        @focus="handleActiveLabel"
        @blur="handleDeactiveLabel"
      />
      <span class="label" :class="{ active: activeLabel }">Título</span>
    </div>
  </div>
</template>

<style scoped>
.input-container {
  height: 24px;
  width: 100%;
}
.input {
  height: 100%;
  width: 100%;
  border: none;
  border-bottom: 2px solid var(--primary-color);
  font-size: 16px;
  font-family: Roboto;
  line-height: 24px;
  outline: none;
}

.input:focus {
  line-height: 24px;
  border-bottom: 2.8px solid var(--primary-color);
  transition-duration: 0.2s;
}

.label {
  transition-duration: 0.3s;
  transition-timing-function: ease-in-out;
  position: absolute;
  top: 0;
  left: 0;

  color: rgba(0, 0, 0, 0.38);
  font-family: Roboto;
  font-size: 16px;
}

.active {
  transition-duration: 0.3s;
  transition-timing-function: ease-in-out;

  top: -24px;
  color: blue;
  font-size: 12px;
}
</style>
