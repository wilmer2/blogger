<template>
  <div class="p-relative">
    <div class="menu-icon-container">
      <span class="material-symbols-outlined menu-icon"> more_vert </span>
    </div>

    <div class="option-icon-container">
      <div class="option-icon">
        <span class="material-symbols-outlined"> dangerous </span>
      </div>
      <div class="option-icon">
        <span class="material-symbols-outlined"> report </span>
      </div>
      <div class="option-icon">
        <span class="material-symbols-outlined"> delete </span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.menu-icon {
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

@media (width >= 768px) {
  .menu-icon-container {
    display: none;
  }
}
</style>
