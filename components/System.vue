<template>
  <Card>
    <h2 class="text-5xl font-bold pb-2">System</h2>
    <div>
      <table>
        <tr>
          <td>Pump</td>
          <td>
            <Select dataKey="pump" />
          </td>
        </tr>
        <tr>
          <td>Bed #1 Solenoid</td>
          <td>
            <Select dataKey="solenoidOne" />
          </td>
        </tr>
        <tr>
          <td>Bed #2 Solenoid</td>
          <td>
            <Select dataKey="solenoidTwo" />
          </td>
        </tr>
        <tr>
          <td>Spray Duration</td>
          <td>
            <Input dataKey="sprayDuration" unit="s" />
          </td>
        </tr>
        <tr>
          <td>Spray Interval</td>
          <td>
            <Input dataKey="sprayInterval" unit="m" />
          </td>
        </tr>
        <tr>
          <td>Forecast</td>
          <td>70% chaince of rain after 15:00.</td>
        </tr>
      </table>
    </div>
  </Card>
</template>

<script lang="ts">
import Vue from 'vue'
import Card from '../components/Card.vue';
import Select from '../components/Select.vue';
import Input from '../components/Input.vue';

export default Vue.extend({
  name: 'System',
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
</style>
