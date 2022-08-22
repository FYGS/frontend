<template>
  <n-link :to="{ name: 'details-slug', params: { slug: item.slug } }">
    <div class="container" @mouseover="onMouseOver" @mouseleave="onMouseLeave">
      <img :src="item.image" :alt="item.subtitle" class="image image-cover" />
      <div class="overlay">
        <div class="text-header">
          <div class="subtitle">{{ subtitle }}</div>
          <div class="title">{{ title }}</div>
        </div>
        <transition-group
          name="bounce"
          tag="div"
          :class="displayable() ? 'show' : 'hide'"
          class="description"
        >
          <div key="description" class="description-text">
            {{ `${item.description.substring(0, 100)}...` }}
          </div>
          <button v-if="!isFirstItem" key="more" class="description-button">
            Explore More
          </button>
        </transition-group>
      </div>
    </div>
  </n-link>
</template>

<script lang="ts">
import Vue from 'vue'
import { DataType } from '~/data'

export default Vue.extend({
  props: {
    item: {
      type: Object as () => DataType,
      required: true,
    },
    isFirstItem: {
      type: Boolean,
      required: false,
      default: false,
    },
  },
  data() {
    return {
      hovered: false,
    }
  },
  computed: {
    subtitle(): string {
      return this.item.subtitle.toUpperCase()
    },
    title(): string {
      return this.isFirstItem
        ? this.item.title.toLowerCase()
        : this.item.title.toUpperCase()
    },
  },
  methods: {
    onMouseOver() {
      this.hovered = true
    },
    onMouseLeave() {
      this.hovered = false
    },
    displayable() {
      return this.hovered || this.isFirstItem
    },
  },
})
</script>
<style scoped>
/* Container needed to position the overlay. Adjust the width as needed */
.container {
  position: relative;
  max-width: 100%;
  height: 400px;

  /* margin: 1.2rem; */
  color: white;
  border-radius: 8px;

  /* box-shadow: 0 4px 8px 0 rgb(0 0 0 / 20%); */

  /* max-width: 650px; */
}

.text-header {
  color: white;
  padding: 10px;
}

.subtitle {
  font-size: 1rem;
}

.description {
  text-align: center;
  font-size: 1rem;
}

.description-text {
  margin: 1.2rem;
}

.description-button {
  background-color: transparent;
  color: white;
  padding: 1rem 2rem;

  /* text-align: center; */
  text-decoration: none;

  /* display: inline-block; */

  /* font-size: 16px; */
  margin: 4px 2px;
  cursor: pointer;
  border: 2px solid white;
  border-radius: 5px;
}

.show {
  display: '';
}

.hide {
  display: none;
}

.title {
  font-size: 2rem;
  font-weight: bold;
}

/* The overlay effect - lays on top of the container and over the image */
.overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #f1f1f1;
  font-size: 1.2rem;
  padding: 1.2rem 0;
  text-align: center;
}

.container:hover .image {
  opacity: 0.8;
  animation: bounce-in 0.5ms;
}

/* Transition */
.bounce-enter-active {
  animation: bounce-in 0.5s;
}

@keyframes bounce-in {
  0% {
    transform: scale(0);
  }

  50% {
    transform: scale(1.25);
  }

  100% {
    transform: scale(1);
  }
}
</style>
