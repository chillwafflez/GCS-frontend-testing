<template>
<div>This is from parent component: {{ percentage }}</div>

<div class="outer_div">
    <div class="container">
        <div class="battery_section" id="section_1"></div>
        <div class="battery_section" id="section_2"></div>
        <div class="battery_section" id="section_3"></div>
        <div class="battery_section" id="section_4"></div>
    </div>
    <div class="battery_widget"></div>
    <img src="..\assets\lightning-icon-png-5.png" id="battery_icon">
</div>

<div class="outer_div_2">
    <br>
    <div class="container_2">
        <div class="battery_section section_1_2"></div>
        <div class="battery_section section_2_2"></div>
        <div class="battery_section section_3_2"></div>
        <div class="battery_section section_4_2"></div>
    </div>
    <div class="battery_widget_2"></div>
    <img src="..\assets\lightning-icon-png-5.png" id="battery_icon_2">
</div>

</template>

<script lang="ts">
    function resetBattery() {
        document.getElementById("battery_icon").style.visibility = "hidden" 
        document.getElementById("section_1").style.visibility = "visible"
        document.getElementById("section_2").style.visibility = "visible"
        document.getElementById("section_3").style.visibility = "visible"
        document.getElementById("section_4").style.visibility = "visible"
        document.getElementById("section_1").style.width = "100%";
        document.getElementById("section_1").style.backgroundColor = "rgb(116, 194, 92)"
        document.getElementById("section_2").style.backgroundColor = "rgb(116, 194, 92)"
        document.getElementById("section_3").style.backgroundColor = "rgb(116, 194, 92)"
        document.getElementById("section_4").style.backgroundColor = "rgb(116, 194, 92)"
    }

    export default {
        data() {
            return {
                critical: 0
            };    
        },
        props: {
            percentage: { required: true, type: Number}
        },
        watch: {
            percentage: function() {
                console.log("COCOOCOCOCOOK")
                resetBattery();
                if (this.percentage == -1) {
                    console.log("bruh")
                } else if (this.percentage <= 10) {
                    document.getElementById("section_1").style.backgroundColor = "red";
                    document.getElementById("section_1").style.width = "50%";
                    document.getElementById("battery_icon").style.visibility = "visible"

                    document.getElementById("section_2").style.visibility = "hidden";
                    document.getElementById("section_3").style.visibility = "hidden"; 
                    document.getElementById("section_4").style.visibility = "hidden"; 
                } else if (this.percentage <= 25) {
                    document.getElementById("section_1").style.backgroundColor = "gray";
                    document.getElementById("section_2").style.visibility = "hidden";
                    document.getElementById("section_3").style.visibility = "hidden"; 
                    document.getElementById("section_4").style.visibility = "hidden"; 
                } else if (this.percentage <= 50) {
                    document.getElementById("section_1").style.backgroundColor = "rgb(245, 225, 44)";
                    document.getElementById("section_2").style.backgroundColor = "rgb(245, 225, 44)";
                    document.getElementById("section_3").style.visibility = "hidden"; 
                    document.getElementById("section_4").style.visibility = "hidden"; 
                } else if (this.percentage <= 75) {
                    document.getElementById("section_4").style.visibility = "hidden"; 
                }
            }
        },
        computed: {
            percentageStatus() {

            }
        },
        methods: {
            makeBattery50() {
                document.getElementById("section_1").style.backgroundColor = "rgb(245, 225, 44)";
                document.getElementById("section_2").style.backgroundColor = "rgb(245, 225, 44)";
                document.getElementById("section_3").style.visibility = "hidden"; 
                document.getElementById("section_4").style.visibility = "hidden"; 
            },
            makeBattery25() {
                document.getElementById("section_1").style.backgroundColor = "gray";
                document.getElementById("section_2").style.visibility = "hidden";
                document.getElementById("section_3").style.visibility = "hidden"; 
                document.getElementById("section_4").style.visibility = "hidden"; 
            },
            makeBattery10() {
                document.getElementById("section_1").style.backgroundColor = "red";
                document.getElementById("section_1").style.width = "50%";
                document.getElementById("battery_icon").style.visibility = "visible"

                document.getElementById("section_2").style.visibility = "hidden";
                document.getElementById("section_3").style.visibility = "hidden"; 
                document.getElementById("section_4").style.visibility = "hidden"; 
            }
            ,
            changeText() {
                document.getElementById("p_tag").innerHTML = "changeText() function was called! HOLLOW PURPLE"; 
                console.log("YIPPEEE");
            }
        },
    };
</script>


<style>
/* FIRST BATTERY ICON */
    .outer_div {
        position: relative;
        /* width: 30%; */
        height: 110px;
        width: 225px;    
    }

    .container {
        position: relative;
        display: flex;
        border: 0.4em solid black;
        /* height: 110px;
        width: 225px; */
        height: 100%;
        width: 100%;
        border-radius: 20px;
        background-color: white;
    }

/* Each battery segment */
    .battery_section {
        width:100%;
        height:92%;
        background-color: rgb(116, 194, 92);
        margin-top: 2%;
        margin-bottom: 2%;
    }
    #section_1 {
        border-radius: 12px 0 0 12px;
        margin-left: 2%;
        visibility: visible;
    }
    #section_2 {
        margin-left: 2%;
        margin-right: 2%;
        visibility: visible;
    }
    #section_3 {
        margin-right: 2%;
        visibility: visible;
    }
    #section_4 {
        border-radius: 0 12px 12px 0;
        margin-right: 2%;
        visibility: visible;
    }

    .battery_widget {
        position: absolute;
        height: 50%;
        width: 20px; 
        background-color:black; 
        left: 242px;
        top: 30%;
        border-radius: 0 12px 12px 0;
    }

    #battery_icon {
        position: absolute;
        width: 40%;
        left: 34%;
        top: 15%;
        animation: blinker 1s linear infinite;
        visibility: hidden;
    }


/* SECOND BATTERY ICON */
    .outer_div_2 {
        position: relative;
        /* width: 30%; */
        height: 110px;
        width: 225px;
    }

    .container_2 {
        position: relative;
        display: flex;
        border: 0.4em solid black;
        /* height: 110px;
        width: 225px; */
        height: 100%;
        width: 100%;
        border-radius: 20px;
        background-color: white;
    }

/* Each battery segment */
    .battery_section_2 {
        width:100%;
        height:92%;
        background-color: rgb(116, 194, 92);
        margin-top: 2%;
        margin-bottom: 2%;
    }
    .section_1_2 {
        border-radius: 12px 0 0 12px;
        margin-left: 2%;
    }
    .section_2_2 {
        margin-left: 2%;
        margin-right: 2%;
    }
    .section_3_2 {
        margin-right: 2%;
    }
    .section_4_2 {
        border-radius: 0 12px 12px 0;
        margin-right: 2%;
    }

    .battery_widget_2 {
        position: absolute;
        height: 50%;
        width: 20px; 
        background-color:black; 
        left: 242px;
        top: 30%;
        border-radius: 0 12px 12px 0;
    }

    #battery_icon_2 {
        position: absolute;
        width: 40%;
        left: 34%;
        top: 30%;
        animation: blinker 1s linear infinite;
    }

    @keyframes blinker {
        50% {
            opacity: 0;
        }
    }
    
</style>
