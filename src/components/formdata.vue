<template>
	<div>
		<input type="text" @input="change" v-model="msg">
		<p>{{message}}</p>
	</div>
</template>
<script>
	export default{
		name:'formdata',
		data(){
			return{
				msg:'hello Vue!!!',
				message:'hello Vue!!!',
				timer:null
			}
		},
		watch:{
			msg(val){
				console.log(2)
				this.timer=setTimeout(()=>{
					this.message=val;	
				},1000)
			}
		},
		methods:{
			change(){
				clearTimeout(this.timer)
			}
		}
	}
</script>
<style></style>