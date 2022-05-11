<template>
	<div>
	<input type= "text" placeholder="firstname" v-model="firstname">
	<input type= "text" placeholder="lastname" v-model="lastname">
	</div>

	<PersonGreeting :firstname ="firstname" :lastname ="lastname" @callHeroes="callHeroes"/>
</template>

<script>

import { ref } from "vue"
import PersonGreeting from "./PersonGreeting.vue"

export default{
	name:"Person",
	components:{
		PersonGreeting,
	},
	setup(){

		const firstname = ref('')
		const lastname = ref('')

		function callHeroes(hero){
			alert(`calling ${hero}`)
		}
		return {
			firstname,
			lastname,
			callHeroes,
		}
	},
	data(){

		return {		
			
		}
	}
}
</script>

<style scope>

</style>