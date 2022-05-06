<template>

	<button @click="getPosts">Load Posts</button>
	<div v-for="post in posts" :key="post.id">
		<h3 v-if="errorMsg">{{errorMsg}}</h3>
		<h2>{{post.id}} , {{post.title}}</h2>
		<p>{{post.body}}</p>
		<hr />
	</div>
</template>

<script>

import axios from "axios"

export default{
	name: "PostLists",
	data(){
		return {
			posts: [],
			errorMsg: '',
		}
	},
	methods: {
		getPosts(){
			axios.get('https://my-json-server.typicode.com/typicode/demo/posts')
			.then((response) => {
				console.log(response.data)
				this.posts = response.data
			})
			.catch(error => {
				console.log(error)
				this.errorMsg= 'Error retrieving data from the source'
			})
		},
	},

}

</script>

<style scope>


</style>