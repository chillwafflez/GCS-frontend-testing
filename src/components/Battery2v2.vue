<!-- Green lit 4 segment one that can adjust to size of outer component -->

<template>

<!-- <div class="outer_div">
    <div class="container">
        <div class="battery_section" id="section_1"></div>
        <div class="battery_section" id="section_2"></div>
        <div class="battery_section" id="section_3"></div>
        <div class="battery_section" id="section_4"></div>
    </div>
    <div class="battery_widget"></div>
    <img src="..\assets\lightning-icon-png-5.png" id="battery_icon">
</div> -->

<div class="outer_div">
    <div class="container">
        <div class="battery_section" id="section_1"></div>
        <div class="battery_section" id="section_2"></div>
        <div class="battery_section" id="section_3"></div>
        <div class="battery_section" :class="fourthSection" id="section_4"></div>
    </div>
    <div class="battery_widget"></div>
    <img src="..\assets\lightning-icon-png-5.png" id="battery_icon">
</div>

</template>

<script lang="ts">
    // function to reset battery css
    function resetBattery() {
        // hides flashing battery symbol
        this.$el.querySelector("#battery_icon").style.visibility = "hidden" 
        // makes all battery segments visible again
        this.$el.querySelector('#section_1').style.visibility = "visible";
        this.$el.querySelector('#section_2').style.visibility = "visible";
        this.$el.querySelector('#section_3').style.visibility = "visible";
        this.$el.querySelector('#section_4').style.visibility = "visible";
        this.$el.querySelector("#section_1").style.width = "100%";
        // changes all battery segments to green
        this.$el.querySelector("#section_1").style.backgroundColor = "rgb(116, 194, 92)"
        this.$el.querySelector("#section_2").style.backgroundColor = "rgb(116, 194, 92)"
        this.$el.querySelector("#section_3").style.backgroundColor = "rgb(116, 194, 92)"
        this.$el.querySelector("#section_4").style.backgroundColor = "rgb(116, 194, 92)"
    }

    export default {
        data() {
            return {
                critical: 0,
                penis: true
            };    
        },
        props: {
            percentage: { required: true, type: Number},
        },
        watch: {
            // percentage: function() {
            //     resetBattery();
            //     if (this.percentage <= 0) {
            //         this.$el.querySelector('#section_1').style.visibility = "hidden";
            //         this.$el.querySelector('#section_2').style.visibility = "hidden";
            //         this.$el.querySelector('#section_3').style.visibility = "hidden";
            //         this.$el.querySelector('#section_4').style.visibility = "hidden";
            //         this.$el.querySelector('#battery_icon').style.visibility = "visible";
            //         // document.getElementById("battery_icon").style.visibility = "visible"
            //     } else if ((this.percentage > 0) && (this.percentage <= 10)) {
            //         this.$el.querySelector('#section_1').style.backgroundColor = "red";
            //         this.$el.querySelector('#section_1').style.width = "50%";
            //         this.$el.querySelector('#battery_icon').style.visibility = "visible";

            //         this.$el.querySelector('#section_2').style.visibility = "hidden";
            //         this.$el.querySelector('#section_3').style.visibility = "hidden";
            //         this.$el.querySelector('#section_4').style.visibility = "hidden";
            //     } else if ((this.percentage > 10) && (this.percentage <= 30)) {
            //         this.$el.querySelector('#section_1').style.backgroundColor = "gray";
            //         this.$el.querySelector('#section_2').style.visibility = "hidden";
            //         this.$el.querySelector('#section_3').style.visibility = "hidden";
            //         this.$el.querySelector('#section_4').style.visibility = "hidden";
            //     } else if ((this.percentage > 30) && (this.percentage <= 60)) {
            //         this.$el.querySelector("#section_1").style.backgroundColor = "rgb(245, 225, 44)";
            //         this.$el.querySelector("#section_2").style.backgroundColor = "rgb(245, 225, 44)";
            //         this.$el.querySelector("#section_3").style.visibility = "hidden"; 
            //         this.$el.querySelector("#section_4").style.visibility = "hidden"; 
            //     } else if ((this.percentage > 60) && (this.percentage <= 75)) {
            //         this.$el.querySelector("#section_4").style.visibility = "hidden"; 
            //     }            
            // }
        },
        // watch: {
        //     percentage: function() {
                // resetBattery();
                // if (this.percentage <= 0) {
                //     document.getElementById("section_1").style.visibility = "hidden";
                //     document.getElementById("section_2").style.visibility = "hidden";
                //     document.getElementById("section_3").style.visibility = "hidden"; 
                //     document.getElementById("section_4").style.visibility = "hidden";
                //     document.getElementById("battery_icon").style.visibility = "visible"
                // } else if ((this.percentage > 0) && (this.percentage <= 10)) {
                //     document.getElementById("section_1").style.backgroundColor = "red";
                //     document.getElementById("section_1").style.width = "50%";
                //     document.getElementById("battery_icon").style.visibility = "visible"
                //     document.getElementById("section_2").style.visibility = "hidden";
                //     document.getElementById("section_3").style.visibility = "hidden"; 
                //     document.getElementById("section_4").style.visibility = "hidden"; 
                // } else if ((this.percentage > 10) && (this.percentage <= 30)) {
                //     document.getElementById("section_1").style.backgroundColor = "gray";
                //     document.getElementById("section_2").style.visibility = "hidden";
                //     document.getElementById("section_3").style.visibility = "hidden"; 
                //     document.getElementById("section_4").style.visibility = "hidden"; 
                // } else if ((this.percentage > 30) && (this.percentage <= 60)) {
                //     document.getElementById("section_1").style.backgroundColor = "rgb(245, 225, 44)";
                //     document.getElementById("section_2").style.backgroundColor = "rgb(245, 225, 44)";
                //     document.getElementById("section_3").style.visibility = "hidden"; 
                //     document.getElementById("section_4").style.visibility = "hidden"; 
                // } else if ((this.percentage > 60) && (this.percentage <= 75)) {
                //     document.getElementById("section_4").style.visibility = "hidden"; 
                // }
        //     }
        // },
        computed: {
            fourthSection() {
                if (this.penis == true) {
                    return 'visibility: hidden'
                }
            }
        },
        methods: {
        },
    };
</script>


<style scoped>
/* FIRST BATTERY ICON */
    .outer_div {
        display: flex;

        position: relative;
        /* height: 110px;
        width: 225px;     */
        height: 12%;
        width: 12%;  
    }

    .container {
        position: relative;
        display: flex;
        border: 0.1em solid black;
        /* height: 110px;
        width: 225px; */
        height: 100%;
        width: 100%;
        /* border-radius: 20px; */
        border-radius: 12%;
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
        /* border-radius: 12px 0 0 12px; */
        border-radius: 15% 0 0 15%;
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
    /* #section_4 {
        border-radius: 0 15% 15% 0;

        margin-right: 2%;
        visibility: visible;
    } */
    .penis {

    }

    .battery_widget {
        position: relative;
        /* height: 50%; */
        height: 50%;
        /* width: 20px; */
        width: 10%;  
        background-color:black; 
        /* left: 242px; */
        top: 30%;
        left: 1%;
        /* top: 30%; */
        /* border-radius: 0 12px 12px 0; */
        border-radius: 0 25% 25% 0;
    }

    #battery_icon {
        position: absolute;
        width: 40%;
        left: 30%;
        top: 15%;
        animation: blinker 1s linear infinite;
        visibility: hidden;
    }

    @keyframes blinker {
        50% {
            opacity: 0;
        }
    }
    
</style>
