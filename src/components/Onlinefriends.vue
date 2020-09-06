<template>
	<div>
		<h2>Posts!!!</h2>

		<input type="text" v-model="search"/>
		<div v-for="post in filtersearch" :key="post.id">
			<h2>{{ post.title }}</h2>
			<p>{{ post.body | snippet}}</p>
		</div>
	</div>
</template>

<script>
	import axios from 'axios'

	export default {
		name: 'Onlinefriends',
		data(){
			return{
				posts: [],
				search: ''
			}	
		},
		computed:{
			filtersearch(){
				return this.posts.filter(post =>{
					return post.title.match(this.search)
					})
				}
		},
		created(){
			axios.get('https://jsonplaceholder.typicode.com/posts')
			.then(response =>{
				this.posts = response.data
			})
			.catch(error=>{
				console.log(error)
			})
		}
	}
</script>

<style>

</style>