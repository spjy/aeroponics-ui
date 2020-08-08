<template>
  <Card>
    <div class="flex flex-row">
      <h2 class="text-5xl font-bold">90{{ unit }}</h2>
      <div class="percent-difference">+2.36%</div>
    </div>
    <p class="-mt-5">{{ dataType }}</p>
    <div>
    </div>
  </Card>
</template>

<script lang="ts">
import Vue from 'vue'
import Card from '../components/Card.vue';
import Select from '../components/Select.vue';

export default Vue.extend({
  name: 'Data',
  props: {
    dataType: {
      type: String,
      required: true,
    },
    dataKey: {
      type: String,
      required: true,
    },
    unit: {
      type: String,
      required: true,
    }
  },
  components: {
    Card,
    Select,
  },
  data() {
    return {
      pump: 'OFF',
      solenoidOne: 'OFF',
      solenoidTwo: 'OFF',
      sprayLength: 10,
      sprayInterval: 10,
      pumpStatus: 'OFF',
    }
  }
})
</script>

<style lang="scss">
table {
  border-spacing: 10px 0;
  border-collapse: separate;
}

tr td:first-child {
  @apply font-bold;
  color: #B7B7B7;
}

select {
  background-color: #393e46;
  margin-left: -4px;
}

input {
  background-color: #393e46;
  white-space: nowrap;
  width: 30px;
}

.percent-difference {
  @apply pl-3;
  @apply text-lg;
  line-height: 5;
  color: #81EFB4;
}
</style>
