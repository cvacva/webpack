<template>
	<div>
		<h1>我是组件1{{message}}</h1>
		<button @click="msg">点击</button>
	</div>
</template>
<script>
	export default{
		data(){
			return{
				message:''
			}
		},
		methods:{
			msg(){
				this.message='我是组件11111111111111'
			}
		}
	}
</script>
<style scoped>
	h1{color:red;}
</style>