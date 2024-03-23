<template>
	<div  id="app">
		<Airspeed :size="350" :airspeed="150"  />
		<Attitude :size="100" :pitch="0" :roll="10" />
	<Attitude  />
	</div>
</template>


<script>
import {Airspeed, Attitude} from  'vue-flight-indicators'

export  default {
	name:  'app',
	components: {
		Airspeed,
		Attitude
	}
}
</script>