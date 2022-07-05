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
  grid-template-columns: 20% calc(80% - 1.5rem);
  gap: 1.5rem;
  margin: 1rem 1.5rem;
  height: calc(100vh - 8rem);

  .entry-content {
    background-color: $background;
    height: calc(100vh - 8rem);
    border-radius: 20px;
    height: 100%;
  }
}
</style>