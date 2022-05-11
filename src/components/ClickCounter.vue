<template>
		<div>
			<button @click="incrementCount">Clicked {{count}} times</button>			
		</div>
</template>

<script>
import useCounter from "./composables/useCounter.js"

export default {
	name:"ClickCounter",
	setup(){
	const {count, incrementCount} = useCounter(100,10)
	
		return{
			count,
			incrementCount,
		}
	
	}

}
</script>
<style scope>

</style>