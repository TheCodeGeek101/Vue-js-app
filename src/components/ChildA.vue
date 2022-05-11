<template>
	<h2>Child component A </h2>
	<ChildB />
</template>

<script>
import ChildB from './ChildB.vue'
export default{
	name:"ChildB",
	components:{
		ChildB,
	}
}
</script>

<style scope>

</style>