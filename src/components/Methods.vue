 <template>
		<div>
			<h2>
				{{name}}
			</h2>
			<button @click="setName">Change name</button>
			<h2>{{count}}</h2>
			<button @click="incrementCount">increment Count</button>
			
			<h2>{{firstname}}  {{lastname}}</h2>
			<button @click="changeHero">Change Hero</button>
		</div>
</template>

<script>

import { ref, reactive, toRefs } from "vue"

export default{
	name:"Methods",
	setup(){
		const count = ref(0)
		const state = reactive({
			firstname : "Bruce",
			lastname :"Wayne"
		})
	   function incrementCount(){
		   count.value++
	   }
	   function changeHero(){
		   state.firstname = "clark"
		   state.lastname = "kent"
	   }

	   return {
		   count,
		   incrementCount,
		   ...toRefs(state),
		   changeHero, 
	   }
	},
	data(){
		return {		
			name:"Themba",
		}
	},
	methods: {
		setName(){
			this.name = "Thembinkosi"
		}
	}
}
</script>

<style scope>

</style>