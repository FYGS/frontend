<template>
  <footer class="center">{{ title }}</footer>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      title: 'Copyrigths 2022',
    }
  },
})
</script>
<style scoped>
footer {
  background-color: #333;
  margin-top: 1.5rem;
  color: #fff;
  text-align: center;
  font-size: 0.8rem;
  padding: 15px;
}
</style>
