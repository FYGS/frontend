<template>
  <div class="row">
    <div v-if="items.length === 0" class="text-center">Missing items !</div>
    <div v-else-if="items.length < 7" class="text-center">
      Waiting for exactly 7 items ! Please check the fetched items !
    </div>

    <div v-else>
      <!-- Line One -->
      <grid-item
        :item="items[0]"
        :is-first-item="true"
        class="col-xs-12"
      ></grid-item>
      <!-- End line One -->

      <!-- Line Two -->
      <grid-item
        :item="items[1]"
        :is-first-item="false"
        class="col-s-12 col-l-6"
      ></grid-item>
      <grid-item
        :item="items[2]"
        :is-first-item="false"
        class="col-s-12 col-l-3"
      ></grid-item>
      <grid-item
        :item="items[3]"
        :is-first-item="false"
        class="col-s-12 col-l-3"
      ></grid-item>
      <!-- End line Two -->

      <!-- Line Three -->
      <grid-item
        :item="items[4]"
        :is-first-item="false"
        class="col-s-12 col-l-3"
      ></grid-item>
      <grid-item
        :item="items[5]"
        :is-first-item="false"
        class="col-s-12 col-l-3"
      ></grid-item>
      <grid-item
        :item="items[6]"
        :is-first-item="false"
        class="col-s-12 col-l-6"
      ></grid-item>
      <!-- End line Three -->
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { DataType } from '~/data'

export default Vue.extend({
  props: {
    items: {
      type: Array as () => DataType[],
      required: true,
    },
  },
})
</script>
