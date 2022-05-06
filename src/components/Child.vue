<template>

	<h2>Portal content</h2>

</template>

<script>

export default{
	name: "Child",
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