<template>
		<div>
			<h1 @mouseover="incrementCount">Hovered {{count}} times</h1>			
		</div>
</template>

<script>

import CounterMixin from '../mixins/counter.js'
import useCounter from './composables/useCounter.js'

export default {
	name:"HoverCounter",
	setup(){
	
		const { count , incrementCount } = useCounter(100,10)

		return {
			count,
			incrementCount,	
		}
	},
	
}
</script>
<style scope>

</style>