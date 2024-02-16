<script lang="ts">

// function updateBattery() {
//     // let percent = "20%"
//     document.getElementById('battery_progress').style.width = "20%";
//     document.getElementById('percentage').innerHTML = "20%";
// }
</script>


<template>
    <button onclick="updateBattery()">Change battery</button>

    <div class="battery_container">
        <div class="battery">
            <div id="battery_progress">
                <div class="percentage">80%</div>
            </div>
        </div>
    </div>

    <!-- <h1>Second battery</h1>
    <div class="battery_container">
        <div class="battery">
            <progress value="50" max="100"></progress>
        </div>
    </div> -->

</template>

<style>
    .battery_container {
        border: 0.4em solid black;
        height: 110px;
        width: 225px;
        border-radius: 20px;
    }

    .battery {
        position: relative;
        height: 86%;
        margin: 2%;
    }

    #battery_progress {
        background-color: rgb(116, 194, 92); 
        color: white; 
        padding: 1%; 
        text-align: center; 
        font-size: 2em; 
        border-radius: 15px; 
        height:100%;
        width: 80%; 
    }

    .percentage {
        margin-top: 15%;
        position: relative;
    }

    progress {
        background-color: pink;
        height: 100%;
        width: 100%;
        border-radius: 20px;
    }

</style>
