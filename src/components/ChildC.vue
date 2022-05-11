<template>

	<h2>Child component C </h2>
	<h3>Child Component C username - {{ userName }}</h3>
	<h3>Child Component C compostion username - {{ childUsername }}</h3>

	<h3>Child Component C count - {{ childCount }} </h3>
	<h3>Child Component C hero - {{ firstName }} {{lastName}} </h3>

</template>

<script>
import {inject, toRefs} from "vue"

export default{
	name:"ChildC",
	inject: ['userName'],
	setup(){
		const childCount = inject('c_count',0)
		const childhero = inject('c_hero', {})

		const childUsername = inject('c_userName','Default username')

		return{
			childUsername,
			childCount,
			...toRefs(childhero)
		}
	}

}
</script>

<style scope>

</style>