<template>
  <span class="material-symbols-outlined menu-icon"> more_vert </span>
  <div class="avatar-container d-none p-relative">
    <span class="avatar-name">Sangel</span>
    <div class="avatar-options d-none">
      <div class="icon-option">
        <span class="material-symbols-outlined"> send_and_archive </span>
      </div>
      <div class="icon-option">
        <span class="material-symbols-outlined"> label </span>
      </div>
      <div class="icon-option">
        <span class="material-symbols-outlined"> delete </span>
      </div>
      <div class="icon-option">
        <span class="material-symbols-outlined"> visibility </span>
      </div>
    </div>
    <span class="material-symbols-outlined letter-icon"> account_circle </span>
  </div>
</template>

<style scoped>
@media (width >= 600px) {
  .menu-icon {
    display: none;
  }

  .avatar-container {
    display: flex;
    align-items: center;
  }

  .avatar-name {
    margin-right: 4px;
  }

  .avatar-options {
    position: absolute;
    left: -170px;
    top: -2px;
  }

  .icon-option span {
    color: #37474f;
  }

  .icon-option {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 30px;
    width: 30px;
    margin-left: 10px;

    border-radius: 50%;
  }

  .icon-option:hover {
    background-color: #eceff1;
  }
}
</style>
