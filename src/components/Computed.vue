<template>
		<div>
			<input type ="text" placeholder="First Name" v-model="fname" >
			<input type ="text" placeholder="Last Name" v-model="lname" >

		<h2> Options - {{ fullname }}</h2>
			
			<input type ="text" placeholder="First Name" v-model="refFirstname" >
			<input type ="text" placeholder="Last Name" v-model="refLastname" >
		
		<h2>Composition fullname is {{refFullname}} </h2>

			<input type ="text" placeholder="First Name" v-model="reactiveFirstname" >
			<input type ="text" placeholder="Last Name" v-model="reactiveLastname" >
		
		<h2>Reactive fullname is {{reactiveFullname}}</h2>
		</div>
</template>

<script>

import { ref, computed, reactive, toRefs } from "vue"

export default{
	name:"Computed",
	setup(){
		const refFirstname = ref('')
		const refLastname = ref('')

		const refFullname = computed(function()
		{
			return `${refFirstname.value} ${refLastname.value}`
		})

		const state = reactive({
			reactiveFirstname: '',
			reactiveLastname: '',
		})
		const reactiveFullname = computed(function(){
			return `${state.reactiveFirstname} ${state.reactiveLastname}`
	})
		return {
			refFirstname,
			refLastname,
			refFullname,
			...toRefs(state),
			reactiveFullname 
		}
	},
	data(){	
		return {		
			fname: '',
			lname: '',
		}
	},
	computed: {
	   fullname(){
		 return `${this.fname} ${this.fname}`
		},
	}
}
</script>

<style scope>

</style>