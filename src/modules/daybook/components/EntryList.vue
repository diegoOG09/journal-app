<template>
  <div class="entry-list">
    <div>
      <input
        type="text"
        class="form-control"
        placeholder="Buscar entrada"
      >
    </div>

    <div class="entry-scrollarea">
      <EntryElement v-for="item in 100" :key="item" />
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from 'vue'
export default {
  components: {
    EntryElement: defineAsyncComponent(() => import ('./EntryElement.vue'))    
}
}
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';
.entry-list {
  height: calc(100vh - 10rem);
  border-radius: 20px;
  padding: 1rem 1.5rem;
  // width: 15rem;
  background-color: $background;
}

.entry-scrollarea {
  padding: .5rem 0;
  height: calc(100vh - 13.5rem);
  overflow-y: scroll;
}

</style>