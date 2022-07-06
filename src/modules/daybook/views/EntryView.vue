<template>
  <div class="entry-heading">
    <div class="entry-title">
      <span>15</span>
      <span>Julio</span>
      <span>2022, Jueves</span>
    </div>

    <div>
      <button id="upload">Subir foto <i class="fa-solid fa-image"></i></button>
      <button id="delete">Borrar <i class="fa-solid fa-trash-can"></i></button>
    </div>
  </div>

  <div>
    <textarea id="textarea" placeholder="¿Qué sucedió hoy?" cols="30" rows="10"></textarea>
  </div>

  <AddBtn icon="fa-floppy-disk"/>
</template>

<script>
import { defineAsyncComponent } from 'vue';
export default {
  components: {
    AddBtn: defineAsyncComponent(() => import('../components/AddBtn.vue'))
  }
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.entry-heading {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.entry-title {
  display: inline-block;
  background-color: $purple-light;
  border: 1px solid $main;
  border-radius: 7px;
  padding: 0.8rem 3rem;
  color: $main;
}
#textarea {
  margin: 2rem 0 2rem 0;
  background-color: $background;
  border: none;
  resize: none;
  outline: none;
  color: $title;
  width: 100%;
  height: calc(100vh - 13.7rem);
  font-size: 1.5rem;
}
#delete {
  cursor: pointer;
  background-color: $dark-red;
  border: none;
  padding: 0.6rem 1rem;
  border-radius: 7px;
  color: $red;
  margin-left: 1rem;
}
#upload {
  cursor: pointer;
  background-color: $dark-orange;
  border: none;
  padding: 0.6rem 1rem;
  border-radius: 7px;
  color: $orange;
}
</style>