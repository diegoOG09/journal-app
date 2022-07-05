<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <h1>Hola mundo</h1>

    <button @click="goToDaybook">Primary</button>
    <button @click="goToDaybook">Secondary</button>
    <button @click="goToDaybook">Succes</button>
  </div>
</template>

<script>
export default {
  methods: {
    goToDaybook() {
    this.$router.push({ name: "no-entry" });
    },
  },
};
</script>