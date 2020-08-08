<template>
  <div>
    <System />
    <br />
    <Data dataKey="temperature" dataType="Temperature" unit="˚F" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import System from '../components/System.vue';
import Data from '../components/Data.vue';

export default Vue.extend({
  components: {
    System,
  }
})
</script>

<style lang="scss">
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
html {
  @apply font-body;
}

body {
  background-color: #222831;
  color: white;
  @apply p-5;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
