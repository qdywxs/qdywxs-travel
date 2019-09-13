<template>
  <div>
    <div class="home">Home</div>
    <router-link to="/list" class="home">List</router-link>
  </div>

</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
.home {
  font-size: 2em;
}
</style>
