<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <main>
    <grid-item-list :items="items"></grid-item-list>
  </main>
</template>

<script lang="ts">
import Vue from 'vue'
import { data } from '~/data/db'

export default Vue.extend({
  data() {
    return {
      items: data,
    }
  },
})
</script>
<style>
* {
  box-sizing: border-box;
}

main {
  max-width: 90%;
  margin: auto;
}

.image {
  width: 100%;
  height: 100%;
  border-radius: 8px;
}

.image-cover {
  object-fit: cover;
}

/* Responsiveness */

.row::after {
  content: '';
  clear: both;
  display: table;
}

[class*='col-'] {
  float: left;
  padding: 5px;

  /* For mobile phones: */
  width: 100%;
}

.text-center {
  color: black;
  text-align: center;
  font-size: 1.2rem;
  font-weight: bolder;
}

/* Extra small devices (phones, 375px and down) */
@media only screen and (max-width: 375px) {
  .col-xs-1 {
    width: 8.33%;
  }

  .col-xs-2 {
    width: 16.66%;
  }

  .col-xs-3 {
    width: 25%;
  }

  .col-xs-4 {
    width: 33.33%;
  }

  .col-xs-5 {
    width: 41.66%;
  }

  .col-xs-6 {
    width: 50%;
  }

  .col-xs-7 {
    width: 58.33%;
  }

  .col-xs-8 {
    width: 66.66%;
  }

  .col-xs-9 {
    width: 75%;
  }

  .col-xs-10 {
    width: 83.33%;
  }

  .col-xs-11 {
    width: 91.66%;
  }

  .col-xs-12 {
    width: 100%;
  }
}

/* Small devices (portrait tablets and large phones, 375px and up) */
@media only screen and (min-width: 375px) {
  .col-s-1 {
    width: 8.33%;
  }

  .col-s-2 {
    width: 16.66%;
  }

  .col-s-3 {
    width: 25%;
  }

  .col-s-4 {
    width: 33.33%;
  }

  .col-s-5 {
    width: 41.66%;
  }

  .col-s-6 {
    width: 50%;
  }

  .col-s-7 {
    width: 58.33%;
  }

  .col-s-8 {
    width: 66.66%;
  }

  .col-s-9 {
    width: 75%;
  }

  .col-s-10 {
    width: 83.33%;
  }

  .col-s-11 {
    width: 91.66%;
  }

  .col-s-12 {
    width: 100%;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .col-m-1 {
    width: 8.33%;
  }

  .col-m-2 {
    width: 16.66%;
  }

  .col-m-3 {
    width: 25%;
  }

  .col-m-4 {
    width: 33.33%;
  }

  .col-m-5 {
    width: 41.66%;
  }

  .col-m-6 {
    width: 50%;
  }

  .col-m-7 {
    width: 58.33%;
  }

  .col-m-8 {
    width: 66.66%;
  }

  .col-m-9 {
    width: 75%;
  }

  .col-m-10 {
    width: 83.33%;
  }

  .col-m-11 {
    width: 91.66%;
  }

  .col-m-12 {
    width: 100%;
  }
}

/* Large devices (laptops/desktops, 1024 and up) */
@media only screen and (min-width: 1024px) {
  .col-l-1 {
    width: 8.33%;
  }

  .col-l-2 {
    width: 16.66%;
  }

  .col-l-3 {
    width: 25%;
  }

  .col-l-4 {
    width: 33.33%;
  }

  .col-l-5 {
    width: 41.66%;
  }

  .col-l-6 {
    width: 50%;
  }

  .col-l-7 {
    width: 58.33%;
  }

  .col-l-8 {
    width: 66.66%;
  }

  .col-l-9 {
    width: 75%;
  }

  .col-l-10 {
    width: 83.33%;
  }

  .col-l-11 {
    width: 91.66%;
  }

  .col-l-12 {
    width: 100%;
  }
}

/* Extra large devices (large laptops and desktops, 1280px and up) */
@media only screen and (min-width: 1280px) {
  .col-xl-1 {
    width: 8.33%;
  }

  .col-xl-2 {
    width: 16.66%;
  }

  .col-xl-3 {
    width: 25%;
  }

  .col-xl-4 {
    width: 33.33%;
  }

  .col-xl-5 {
    width: 41.66%;
  }

  .col-xl-6 {
    width: 50%;
  }

  .col-xl-7 {
    width: 58.33%;
  }

  .col-xl-8 {
    width: 66.66%;
  }

  .col-xl-9 {
    width: 75%;
  }

  .col-xl-10 {
    width: 83.33%;
  }

  .col-xl-11 {
    width: 91.66%;
  }

  .col-xl-12 {
    width: 100%;
  }
}
</style>
