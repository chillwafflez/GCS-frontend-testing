<!-- <script setup> -->
<script setup>
// import Battery from './components/Battery.vue';
// import Battery2 from './components/Battery2.vue';
import Battery3 from './components/Battery3.vue';
import Battery4 from './components/Battery4.vue';
import Battery2v2 from './components/Battery2v2.vue';
import Connection from './components/Connection.vue';
import Status from './components/StatusWidget.vue';
import NavBar from './components/NavBarGCS.vue';


</script>

<template>
  <NavBar></NavBar>
  <Status :vehicle-name="'ERU'" />



  <!-- <h2>Below is the Connection component</h2>
  <div class="bruh">
    <Connection :latency=100 />
  </div> -->


  <!-- <h2>Below is the Battery2 component</h2>
  <div class="bruh">
    <Battery4 :percentage=50 :charging="false"/>
  </div> -->

  <!-- <h2>Below is the Battery4 component</h2>
  <div class="bruh">
    <Battery4 :percentage=50 :charging="false"/>
  </div> -->

  <!-- <h2>Below is the Battery2v2 component</h2>
  <div class="bruh">
    <Battery2v2 :percentage=60 />
  </div> -->



</template>

<style scoped>

.bruh {
  /* display: flex; */
  border: 0.4em solid black;
  height: 200px;
  width: 400px;
  /* height: 100px;
  width: 200px;  */
}

</style>
