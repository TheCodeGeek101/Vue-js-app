<template>
		<div>
			<div v-for="post in posts" :key="posts.id">
			<h3 v-if="errorMsg">{{errorMsg}}</h3>
			<h2>{{post.id}} , {{post.title}}</h2>
				<p>{{post.body}}</p>
			</div>
		</div>
</template>

<script>

import axios from "axios"


export default {
	name:"PostList",
	created(){
		this.getPosts()
	},
	data(){
		return{
			Posts: [],
			errorMsg: '',	
		
		}
	},
	methods:{
		getPosts(){
			axios.get("https://my-json-server.typicode.com/typicode/demo/posts")
			.then((response) => {
			console.log(response.data)
			this.posts = response.data
			})
			.catch(error => {
			console.log(error)
			this.errorMsg = "Error retrieving data from the api"
			})
		}
	}
}
</script>
<style scope>

</style>