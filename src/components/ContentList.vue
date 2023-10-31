<script setup lang="ts">
import Select from './Select.vue'

const handleAddTag = (): void => {
  console.log('*** show tag ***')
}
</script>

<template>
  <div class="card-list-header">
    <div class="select-container">
      <Select />
    </div>
    <div class="d-flex p-relative">
      <div class="label-icon-container" @click="handleAddTag">
        <span class="material-symbols-outlined"> label </span>
      </div>
      <div class="filter-label-container">
        <span class="filter-label">ADMINISTRAR</span>
      </div>
    </div>
  </div>

  <div class="card-list">
    <slot></slot>
  </div>
</template>

<style scoped>
.select-container {
  width: 150px;
}

.card-list-header {
  display: flex;
  justify-content: space-between;
  padding: 24px;
}

.filter-label-container {
  margin-left: 16px;
  padding-top: 2px;
  cursor: pointer;
}

.filter-label {
  color: var(--green-color);
  font-size: 14px;
  font-weight: 500;
}

.label-icon-container {
  position: absolute;
  top: -7px;
  left: -40px;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 40px;
  width: 40px;
  border-radius: 50%;
  cursor: pointer;
}

.label-icon-container:hover {
  background-color: var(--hover-icon-color);
}

@media (width >= 1024px) {
  .card-list {
    padding-left: 16px;
    padding-right: 16px;
  }
}
</style>
