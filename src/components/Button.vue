<template>
  <button>
    <span class="material-symbols-outlined"> send </span>
    <span class="letter">Publicar</span>
  </button>
</template>

<style scoped>
button {
  display: flex;
  align-items: center;
  padding: 6px 8px;
  background-color: #f57c00;
  color: white;
  border: none;
  border-radius: 2px;
  font-size: 14px;
  font-weight: 500;
  cursor: pointer;
}
.letter {
  display: none;
  margin-left: 6px;
  font-size: 14px;
  font-weight: 600;
}

@media (width > 840px) {
  .letter {
    display: inline;
  }
}
</style>
