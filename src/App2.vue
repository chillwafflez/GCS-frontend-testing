<!-- <script setup> -->
<script setup>
// import Battery from './components/Battery.vue';
import Battery2 from './components/Battery2.vue';


</script>

<template>
  <button @click="$refs.first_battery2_comp.changeText()">Change text</button>
  <button @click="$refs.first_battery2_comp.makeBattery50()">Make battery icon at 50%</button>
  <button @click="$refs.first_battery2_comp.makeBattery25()">Make battery icon at 25%</button>
  <button @click="$refs.first_battery2_comp.makeBattery10()">Make battery icon at 10%</button>


  <h1>Below is the Battery2 component</h1>
  <Battery2 ref="first_battery2_comp" />

</template>

<style scoped>

</style>
