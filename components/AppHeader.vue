<template>
  <header>
    <div class="nav">
      <n-link to="/">HOME</n-link>
    </div>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>
<style scoped>
header {
  display: flex;
  justify-content: center;
  background-color: #333;
  margin-bottom: 1.5rem;
}

.nav {
  overflow: hidden;
  background-color: #333;
}

.nav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.nav a:hover {
  background-color: #ddd;
  color: black;
}
</style>
