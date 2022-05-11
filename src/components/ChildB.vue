<template>
	<h2>Child component B </h2>
	<ChildC />
</template>

<script>
import ChildC from './ChildC.vue'
export default{
	name:"ChildC",
	components:{
		ChildC,
	}
}
</script>

<style scope>

</style>