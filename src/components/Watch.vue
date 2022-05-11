<template>
	<div>
		<input type ="text" placeholder="name" v-model="name">
		<input type ="text" placeholder="firstname" v-model="firstname">
		<input type ="text" placeholder="lastname" v-model="lastname">
		<input type ="text" placeholder="reactive firstname" v-model="fname">	
		<input type ="text" placeholder="reactive lastname" v-model="lname">
		<input type ="text" placeholder="reactive heroName" v-model="options.heroName">
	</div>
</template>
<script>

import { ref, watch, reactive, toRefs } from "vue"
import _ from 'lodash'

export default {
	name:"Watch",
	setup(){
		const firstname = ref('')
		const lastname = ref('Wayne')

		const state = reactive({
			fname: '',
			lname: '',
			options: {
				heroName: '',
			},
		})

		watch(
		() => _.cloneDeep(state.options),
		function(oldValue,newValue){
			console.log('fname old value',oldValue)
			console.log('fname new value',newValue)
		},
		{
			deep: true
		}
		)

		watch([firstname , lastname], (newValues, oldValues) => {
				
				console.log('first name oldValue',oldValues[0])
				console.log('first name newValue',newValues[0])

				console.log('last name oldValue',oldValues[1])
				console.log('last name newValue',newValues[1])
		},
		 {
			immediate: true,
		})
		return{	
			firstname,
			lastname,
			...toRefs(state)
		}
	},
	data(){
		return {		
			name: '',
		}
	},
	watch:{
		name(newValue, oldValue){
			console.log('oldValue', oldValue)
			console.log('newValue', newValue)
		}
	}
}
</script>

<style scope>

</style>