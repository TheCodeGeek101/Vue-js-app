<template>
	<input type ="text" placeholder="First name" v-model="fname">
	<input type ="text" placeholder="Last name" v-model="lname">
	<input type ="text" placeholder="heroname" v-model="heroname">

	<input type ="text" placeholder="firstName" v-model="firstname">
	<input type ="text" placeholder="lastName" v-model="lastname">	
</template>

<script>
import { ref, reactive, toRefs} from "vue"

export default{

	name:"VModel",
	setup(){
		const heroName = ref('')
		const state = reactive({
			firstname : '',
			lastname: '',

		})
		
		return{	
			heroName,
			...toRefs(state),
		}
	},
	data(){

		return {		
			fname: '',
			lname: '',
		}
	}
}
</script>

<style scope>

</style>