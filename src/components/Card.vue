<script setup lang="ts">
import CardMenu from './CardMenu.vue'
</script>

<template>
  <div class="card-container">
    <div class="card-content d-flex justify-content-between">
      <div class="card-title-container"><span>D</span></div>
      <div class="flex-1 ml-1">
        <div class="d-flex justify-content-between align-items-center card-header">
          <span>Title</span>
          <CardMenu />
        </div>
        <div class="d-flex justify-content-between align-items-center card-publish">
          <div>
            <span class="card-letter d-none card-publish-text"> Publicada </span>
            <span class="card-letter d-none card-publish-text"> • </span>
            <span class="card-letter">27 oct</span>
          </div>
          <div class="d-flex justify-content-between align-items-center">
            <span class="material-symbols-outlined"> share </span>
            <div class="ml-1 d-flex align-items-center">
              <span class="card-letter">0</span>
              <span class="material-symbols-outlined card-publish-icon comment">
                mode_comment
              </span>
            </div>
            <div class="ml-1 d-flex align-items-center">
              <span class="card-letter">0</span>
              <span class="material-symbols-outlined card-publish-icon"> stacked_bar_chart </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card-container {
  margin-bottom: 20px;
  padding: 16px;
  border: 1px solid var(--border-color);
  cursor: pointer;
}

.card-container:hover {
  box-shadow: 1px 1px 6px -1px rgba(168, 171, 172, 0.75);
}

.card-container:hover :deep(.avatar-name) {
  display: none;
}

.card-container:hover :deep(.avatar-options) {
  display: flex;
}

.card-title-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 96px;
  width: 96px;
  border-radius: 5px;
  border: 1px solid var(--border-color);
  color: #78909c;

  font-family: Roboto, sans-serif;
  font-size: 50px;
}

.card-header {
  padding-top: 5px;
}
.card-letter {
  color: #546e7a;
  font-weight: 400;
  font-size: 14px;
}

.card-publish {
  margin-top: 32px;
}

.card-publish-icon {
  margin-left: 5px;
  color: #90a4ae;
  font-size: 14px;
  line-height: 20px;
}

.comment {
  padding-top: 2px;
}

@media (width >= 480px) {
  .card-publish-text {
    display: inline;
  }

  .card-title-container {
    width: 110px;
  }
}

@media (width >= 600px) {
  .card-title-container {
    height: 65px;
    width: 80px;
  }

  .card-publish {
    margin-top: 8px;
  }
}
</style>
