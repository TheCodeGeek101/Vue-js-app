 <template>
		<div>
			<h2>
				{{ state.firstname }} , {{state.lastname}}
			</h2>
		</div>
</template>

<script>

import { reactive } from "vue"

export default{
	name:"DemoTwo",
	setup(){
		const state = reactive({
			firstname: "Bruce",
			lastname: "Wayne",
		})

		setTimeout(() => {
			state.firstname = 'Clark'
			state.lastname = 'Kent'
			console.log(state)

		}, 2000)
		return {
			firstname:state.firstname,
			lastname:state.lastname
		}
	},
	data(){
		return {		
			fname: "Bruce",
			lname: "Wayne"
		}
	}
}
</script>

<style scope>

</style>