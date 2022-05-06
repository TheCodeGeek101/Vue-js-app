<template>

	<h2>Parent content</h2>
	<button @click="showChild = !showChild">Toogle Child</button>
	<Child v-if="showChild" />
</template>

<script>
import Child from './Child.vue'
export default{
	components: {
		Child,
	}
	name: "Parent",
	data(){
		return{
			showChild: true,
		}
	},
	beforeCreated(){
		console.log("chld beforeCreated()")
	},
	created(){
		console.log("child  created()")
	},
	beforeMount(){
		console.log("child beforeMounted()")
	},
	mount(){
		console.log("child  mounted()")
	},
	beforeUpdated(){
		console.log("child beforeUpdated()")
	},
	updated(){
		console.log("child updated()")
	},
	beforeUnmount(){
		console.log("child beforeUnmount()")
	},
	unmount(){
		console.log("child unmounted()")
	}


}
</script>

<style scope>


</style>