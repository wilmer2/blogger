<template>
  <button>
    <span class="material-symbols-outlined"> add </span>
    <span class="btn-str">CREAR ENTRADA</span>
  </button>
</template>

<style scoped>
button {
  display: flex;
  align-items: center;
  padding: 8px 0;
  justify-content: center;
  width: 174px;
  border: none;
  border-radius: 25px;
  background-color: white;
  box-shadow: 1px 1px 6px -1px rgba(168, 171, 172, 0.75);
  color: var(--primary-color);
  cursor: pointer;
}

.btn-str {
  padding-left: 3px;
  color: var(--primary-color);
  font-size: 14px;
  font-family: Roboto !important;
  font-weight: bold !important;
}
</style>
