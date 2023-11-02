<script setup lang="ts">
import Input from './Input.vue'
import PostSelect from './PostSelect.vue'
import Button from './Button.vue'
</script>

<template>
  <div class="d-flex align-items-center post-container">
    <div class="flex-1"><Input /></div>
    <div class="d-flex align-content-start flex-wrap ml-1">
      <div class="mr-1">
        <PostSelect />
      </div>
      <Button />
    </div>
  </div>
</template>

<style scoped>
.post-container {
  padding-left: 10px;
  padding-right: 10px;
}
</style>
