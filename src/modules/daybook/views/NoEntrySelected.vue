<template>
  <div class="no-entry-selected">
    <h1>Selecciona una entrada 👀</h1>
  </div>
  <AddBtn />
</template>

<script>
import { defineAsyncComponent } from "vue";
export default {
  components: {
    AddBtn: defineAsyncComponent(() => import("../components/AddBtn.vue")),
  },
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.no-entry-selected {
  display: block;
  margin-top: 25%;
  text-align: center;
  h1 {
    margin: 0;
    color: $almost-white;
  }
}
</style>