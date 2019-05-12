<template>
  <div>
    <dl>
      <dt>Current Temp</dt>
      <dd>{{ conditions.temp }}</dd>
      <dt>Humidity </dt>
      <dd>{{ conditions.humidity }}%</dd>
      <dt>High </dt>
      <dd>{{ conditions.temp_max }}&deg;F</dd>
      <dt>Low </dt>
      <dd>{{ conditions.temp_min }}&deg;F</dd>
    </dl>
  </div>
</template>

<script>
export default {
  name: 'WeatherConditions',
  data () {
    return {

    }
  },
  props: {
    conditions: {}
  }
}
</script>

<style scoped>
  dl {
    padding: 5px;
    background: #e8e8e8;
  }
  dt {
    float: left;
    clear: left;
    width: 120px;
    text-align: right;
    font-weight: bold;
    color: blue;
    padding: 5px;
  }
  dd {
    margin-top: 5px;
    padding: 0 0 0.5em 0;
  }
  dt::after {
    content: ":";
  }
</style>