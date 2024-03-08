<template>
    <div class="status_container">
        <div > {{ vehicleName }} Status </div>
        <Battery4 :percentage=50 :charging="false"/>
            
    </div>
    
</template>
    
<script lang="ts">
    import Battery from "./StatusComponents/BatteryGCS.vue"

    export default {
        component: {
            Battery
        },
        props: {
            vehicleName: { required: true, type: String},
        },
        computed: {
        },
    };
</script>
    
    
<style scoped>
    .status_container {
        display: flex;
        position: relative;
        height: 40%;
        width: 100%; 
        border: 0.1em solid red;
    }
 

    .battery_container {
        position: relative;
        display: flex;
        border: 0.1em solid black;
        height: 100%;
        width: 100%;
        border-radius: 12%;
        background-color: white;
    }

</style> 