<template>
	<h2> Hello {{fullname}} </h2>
	<button @click ="sendEvent">call heroes</button>
</template>

<script>

import {  computed } from "vue"

export default{
	name:"PersonGreeting",
	setup(props, context){
		
		const fullname = computed(() => {
			return `${props.firstname} ${props.lastname}`
		})

		function sendEvent(){
			context.emit('callHeroes',fullname.value)
		}

		return {
			fullname,
			sendEvent,
		}
	},
	props: ['firstname','lastname'],
	data(){

		return {		
		
		}
	}
}
</script>

<style scope>

</style>