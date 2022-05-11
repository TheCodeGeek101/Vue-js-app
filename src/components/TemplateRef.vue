<template>
		<div>
			<input type = "text" ref="inputRef">
			<PostList ref="postListRef" />
		</div>
</template>

<script>

import axios from "axios"
import PostList from './PostList.vue'

export default {
	name:"TemplateRefs",
	mounted(){
		console.log(this.$refs.postListRef)
		this.$refs.inputRef.focus()
	},
	data(){
		return{
			
		}
	},
	methods:{
	
	}
}
</script>
<style scope>

</style>