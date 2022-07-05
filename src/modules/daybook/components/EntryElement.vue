<template>
  <div class="entry-container" @click="$router.push({name: 'entry', params: {id: 10}})">
    <div class="entry-title">
        <span>15</span>
        <span>Julio</span>
        <span>2021, Jueves</span>
      </div>
    <div class="entry-description">
      Duis amet velit elit minim ad dolore. Aliquip nisi ut do commodo duis ipsum labore laborum magna. Lorem deserunt aliqua eu ipsum dolore proident amet duis id Lorem magna commodo proident. Cupidatat ipsum incididunt labore ipsum cillum amet Lorem. Fugiat consectetur culpa reprehenderit ullamco excepteur officia. Cupidatat Lorem consequat consectetur eiusmod. Minim pariatur ut reprehenderit nostrud sunt duis veniam consectetur adipisicing irure sunt voluptate.
    </div>
  </div>
  
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '@/styles/variables.scss';
.entry-container {
  margin: 1rem 0;
  cursor: pointer;
}
.entry-title {}

</style>