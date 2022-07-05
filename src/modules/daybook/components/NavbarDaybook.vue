<template>
  <nav class="navbar">
    <a href="" class="link-home">
      <img class="logo" src="@/assets/logo.png" alt="Vue Logo">
      Daybook
    </a>

    <div class="logout">
      <button>
        <i class="fa-solid fa-right-from-bracket"></i>
      </button>
    </div>
  </nav>
</template>

<style lang="scss">
@import '@/styles/variables.scss';
.navbar {
  display: flex;
  justify-content: space-between;
  border-radius: 20px;
  background-color: $background;
  margin: 1rem 1.5rem;
  padding: 1rem 1.5rem;
  .link-home {
    display: flex;
    align-items: center;
    gap: 1rem;
    text-decoration: none;
    color: $main;
    font-weight: bold;
    font-size: 2rem;
    img {
      width: 3rem;
    }
  }
  
}
</style>