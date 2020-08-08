<template>
  <span>
    <select @change="handleSelect" v-model="select">
      <option value="" disabled>Mode</option>
      <option value="ON">ON</option>
      <option value="OFF">OFF</option>
    </select>
    <span v-if="value === 'ON'" class="rounded border-solid border border-green-500 px-2 bg-green-500 transition-all duration-300 ease-in-out">ON</span>
    <span v-if="value === 'OFF'" class="rounded border-solid border border-red-500 px-2 bg-red-500 transition-all duration-300 ease-in-out">OFF</span>
  </span>
</template>

<script lang="ts">
import Vue, { PropOptions } from 'vue'

/** Listen to websocket, set value from that */
export default Vue.extend({
  name: 'Select',
  props: {
    dataKey: {
      type: String,
      required: true,
    }
  },
  data() {
    return {
      value: '',
      select: '',
    }
  },
  methods: {
    handleSelect() {
      this.value = this.select;
      this.select = '';
    }
  }
})
</script>

<style>
.card {
  position: relative;
  background-color: #393e46;
  top: 0;
  transition: top ease 0.3s;
  @apply p-5;
}

.card:hover {
  top: -2px;
}
</style>
