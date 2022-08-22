<template>
  <div v-if="currentItem() === undefined">Item Not Found !</div>
  <div v-else>
    <h2 class="d-flex">
      {{ currentItem().title }} - {{ currentItem().subtitle }}
    </h2>
    <div class="container">
      <img
        :src="currentItem().image"
        :alt="currentItem().title"
        class="image image-cover"
      />
    </div>
    <div class="d-flex description">{{ currentItem().description }}</div>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import { DataType } from '~/data'
import { data } from '~/data/db'

export default Vue.extend({
  data() {
    return {
      data,
    }
  },
  methods: {
    currentItem(): DataType | undefined {
      return data.find((item) => item.slug === this.$route.params.slug)
    },
  },
})
</script>
<style scoped>
.container {
  max-width: 100%;
  height: 800px;
  margin: 1.5rem 0;
}

.d-flex {
  display: flex;
  justify-content: center;
}

.description {
  max-width: 80%;
  margin: 1.5rem auto;
}
</style>
