<template>
  <NavbarDaybook />

  <div class="journal-content">
    <div>
      <EntryList />
    </div>
    <div class="entry-content">
      <router-view />
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue'
  export default {
    components: {
    NavbarDaybook: defineAsyncComponent(() => import("../components/NavbarDaybook.vue")),
    EntryList: defineAsyncComponent(() => import("../components/EntryList.vue")),
}
  }
</script>

<style lang="scss">
@import '@/styles/variables.scss';
.journal-content {
  display: grid;
  grid-template-columns: 20% 80%;

  .entry-content {
    background-color: $background;
    height: calc(100vh - 5.4rem);
    padding: 1.5rem 5rem 0 10rem;
  }
}
</style>