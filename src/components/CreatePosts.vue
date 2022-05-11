<template>
		<div>
			<form @submit.prevent="CreatePost">
			<div>
				<label for= "userId">Post Id</label>
				<input type="text" id="userId" v-model="formData.userId">
			</div>
			<div>
				<label for= "title">Post Title</label>
				<input type="text" id="title" v-model="formData.title">
			</div>
			<div>
				<label for= "body">Post Body</label>
				<input type="text" id="body" v-model="formData.body">
			</div>
			</form>
		</div>
</template>
<script>

import axios from "axios"

export default{
	name:"CreatePost",
	data(){
		return{
			formData: {
				userId: '',
				title:'',
				body:'',
			}
		}
	},
	methods:{
		CreatePosts(){
			axios.post("https://my-json-server.typicode.com/typicode/demo/posts",this.formData)
			.then(response =>{
			 	console.log(response)
				 })
			.catch(error => { 
				console.log(error)
			})
		}
	}
}
</script>
<style scope>

</style>