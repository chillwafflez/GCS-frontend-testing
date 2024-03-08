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
  <div class="screen_div">
    <div class="map_div"></div>
    <div class="status_rightside">
        <Status :vehicle-name="'ERU'" />
        <Status :vehicle-name="'MRA'" />
        <Status :vehicle-name="'MEA'" />
        <Status :vehicle-name="'FRA'" />
    </div>
  
  </div>



</template>

<style scoped>

.screen_div {
    display: flex;
    border: 0.003em solid black;
    height: 85vh;
    width: 99vw;
}

.status_rightside {
    display: flex;
    flex-direction: column;
    border: 0.003em solid black;
    height: 100%;
    width: 25%;
    margin-left: auto
}

.map_div {
    background-color: pink;
}



</style>
