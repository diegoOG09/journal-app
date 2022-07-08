<template>
  <div class="entry-list">
    <div class="search">
      <i class="fa-solid fa-magnifying-glass"></i>
      <input
        type="text"
        class="form-control"
        placeholder="Buscar una entrada" 
        v-model="term"
      />
    </div>

    <div class="entry-scrollarea">
      <EntryElement v-for="item in entriesByTerm" :key="item" />
    </div>
  </div>
</template>

<script>
import { defineAsyncComponent } from "vue";
import { mapGetters } from "vuex";
export default {
  components: {
    EntryElement: defineAsyncComponent(() => import("./EntryElement.vue")),
  },
  computed: {
    ...mapGetters('journal', ['getEntriesByTerm']),
    entriesByTerm() {
      return this.getEntriesByTerm(this.term)
    }
  },
  data() {
    return {
      term: ''
    }
  }
};
</script>

<style lang="scss" scoped>
@import "@/styles/variables.scss";
.search {
  display: flex;
  align-items: center;
  gap: .5rem;
  i {
    color: $warm-gray;
  }
}
input {
  display: block;
  width: 80%;
  background-color: transparent;
  padding: 0.6rem 0.5rem;
  border: none;
  border-bottom: 2px solid $warm-gray;
  color: $light-white;
  &:focus,
  input:focus {
    outline: none;
  }
  &:hover {
    
  }
}

.entry-list {
  height: calc(100vh - 5.9rem);
  padding: 1rem 1rem 1rem 1.5rem;
  background-color: $background;
}

.entry-scrollarea {
  padding: 0.5rem 0;
  height: calc(100vh - 10rem);
  overflow-y: scroll;
  &::-webkit-scrollbar {
    display: none;
  }
}
</style>