<template>
  <div class="main-container">
    <div class="container">
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.container {
  margin: 0 auto;
  padding: 24px 12px;
  max-width: 1024px;
}

@media (width >= 1024px) {
  .main-container {
    margin-left: 280px;
  }
}
</style>
