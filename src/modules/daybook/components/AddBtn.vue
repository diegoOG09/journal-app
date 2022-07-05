<template>
  <button>
    <i class="fa-solid fa-circle-plus"></i>
  </button>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';
  button {
    background: none;
    border: none;
    bottom: 20px;
    height: 130px;
    position: fixed;
    right: 20px;
    width: 150px;
    i {
      cursor: pointer;
      color: $main;
      font-size: 4.5rem;
    }
    
  }
</style>