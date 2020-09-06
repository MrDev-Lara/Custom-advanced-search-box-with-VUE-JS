<template>
	<div id="all">
		<h2>All Friends</h2>
		<div v-for="(allfriend,index) in allfriends" :key="index">
			<h2 @click="unfriend(allfriend.name)">{{ allfriend.name }}</h2>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Allfriends',
		props: ['allfriends'],
		data(){
			return{

			}
		},
		methods:{
			unfriend(name){
				this.$emit('delete',(name))
			}
		}
	}
</script>

<style>

</style>