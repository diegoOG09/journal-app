<template>
  <nav class="navbar">
    <a href="" class="link-home">
      <i class="fa-solid fa-newspaper"></i>
      Daybook
    </a>

    <div class="logout">
      <button>
        <i class="fa-solid fa-right-from-bracket"></i>
      </button>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: $background;
  padding: 1rem 1.7rem;
  border-bottom: 2px solid $warm-gray;
  .link-home {
    display: flex;
    align-items: center;
    gap: 1rem;
    text-decoration: none;
    color: $light-white;
    font-weight: bold;
    font-size: 2rem;
    i {
      color: $main;
    }
  }
  button {
    background: none;
    border: none;
    i {
      cursor: pointer;
      font-size: 2rem;
      color: $light-white;
    }
  }
}
</style>