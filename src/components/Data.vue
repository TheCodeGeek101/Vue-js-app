<template>
	<h2> Options - {{o_firstname}}</h2>
	<h2>Composition - {{c_firstName}}</h2>
</template>

<script>

import { ref } from "vue"

export default{
	name:"data",
	setup(){
		const c_firstName = ref('Clark')
		console.log('c_firstName',c_firstName)

		return {
				c_firstName: c_firstName

		}
	},
	data(){

		return {		
			o_firstname: "Bruce"
		}
	}
}
</script>

<style scope>

</style>