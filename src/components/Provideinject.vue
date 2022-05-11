<template>
	<h3>Parent Component  {{name}}</h3>	
		<h3>Parent Component  count {{count}}</h3>
			<h3>Parent Component hero {{firstname}} {{lastname}}</h3>

	<ChildA />
</template>

<script>
import ChildA from  './ChildA.vue'
import {provide, ref, reactive, toRefs} from  'vue'

export default{
	name:"Provideinject",
	data(){
		return {		
			name: 'Thembinkosi',
		}
	},
	setup(){
		provide('c_userName', 'Thembinkosi')

		const count = ref(0)
		const state = reactive({
			firstname: "Bruce",
			lastname: "Wayne"
		})
		
		provide('c_count',count)
		provide('c_hero',state)

		return {
			count,
			...toRefs(state)
		}
	},
	provide(){
		return {
			userName : this.name,
		}
	}
}
</script>

<style scope>

</style>