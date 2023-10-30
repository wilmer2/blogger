<script setup lang="ts">
import CommentCardMenu from './CommentCardMenu.vue'
</script>

<template>
  <div class="main-container">
    <div class="comment-container d-flex">
      <div class="d-flex flex-1 comment-content">
        <figure>
          <img src="@/assets/images/user_blogger.png" alt="Avatar" />
        </figure>
        <div class="comment-info-container ml-1">
          <div class="comment-info-content">
            <div class="comment-publish-container">
              <span class="comment-autor">Wilmer</span> comento en
              <span class="comment-title">"Mi primer cumple"</span>
            </div>
            <div class="comment-date-container">
              <span> 27 oct 2023 </span>
            </div>
          </div>
          <div class="comment-article-container">
            <p class="comment-article">hola no estoy de acuerdo Lorem ipsum dolor sit amet</p>
          </div>
        </div>
      </div>
      <div class="menu-container">
        <CommentCardMenu />
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  margin-bottom: 20px;
  padding: 16px;
  border: 1px solid var(--border-color);
  border-radius: 6px;
  cursor: pointer;
}

.main-container:hover {
  box-shadow: var(--card-shadow);
}

img {
  width: 64px;
  height: 64px;
  border: none;
  border-radius: 50%;
}

.comment-publish-container {
  padding-top: 8px;
  margin-bottom: 10px;
  color: rgba(0, 0, 0, 0.52);
  font-size: var(--font-small);
  font-weight: 400;
}

.comment-article-container {
  margin-top: 10px;
}

.comment-publish-container span {
  color: var(--green-color);
}

.comment-autor {
  font-weight: 500;
}

.comment-date-container {
  color: #546e7a;
  font-weight: 400;
  font-size: var(--font-small);
}

.comment-article {
  color: #37474f;
  letter-spacing: 0.25px;
  line-height: 21px;
}

.menu-container {
  padding-top: 3px;
}

@media (width >= 600px) {
  .comment-content {
    justify-content: flex-start;
  }
  .comment-publish-container {
    padding-top: 0;
    margin-bottom: 0;
  }
  .comment-info-container {
    padding-top: 8px;
    flex: 1;
  }

  .comment-info-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .comment-date-container {
    padding-right: 8px;
  }
}
</style>
