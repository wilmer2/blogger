<template>
  <div class="menu-container">
    <div class="menu-icon-container eye">
      <span class="material-symbols-outlined"> visibility </span>
      <span class="letter-color">Vista previa</span>
    </div>
    <div class="menu-icon-container arrow">
      <span class="material-symbols-outlined"> arrow_drop_down </span>
    </div>
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

@media (width > 840px) {
  .letter-color {
    display: inline-block;
    margin-left: 5px;
    padding-bottom: 1px;
  }
}
</style>
