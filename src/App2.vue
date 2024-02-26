<!-- <script setup> -->
<script setup>
// import Battery from './components/Battery.vue';
import Battery2 from './components/Battery2.vue';
import Battery3 from './components/Battery3.vue';
import Battery4 from './components/Battery4.vue';

</script>

<template>
  <!-- <button @click="$refs.first_battery2_comp.changeText()">Change text</button>
  <button @click="$refs.first_battery2_comp.makeBattery50()">Make battery icon at 50%</button>
  <button @click="$refs.first_battery2_comp.makeBattery25()">Make battery icon at 25%</button>
  <button @click="$refs.first_battery2_comp.makeBattery10()">Make battery icon at 10%</button> -->

  <h2>Below is the Battery4 component</h2>
  <div class="bruh">
    <Battery4 :percentage=10 :charging="false"/>
  </div>

  <h2>Below is the Battery2 component</h2>
  <div class="bruh">
    <Battery2 :percentage=100 ref="first_battery2_comp"/>
  </div>
  <!-- <Battery2 :percentage=70 ref="first_battery2_comp"/> -->
  <!-- <h2>Below is the Battery3 component</h2>
  <Battery3 :percentage_battery3=10 />
   -->

</template>

<style scoped>

.bruh {
  /* display: flex; */
  border: 0.4em solid red;
  height: 200px;
  width: 400px;    
  /* height: 100px;
  width: 200px;  */
}

</style>
