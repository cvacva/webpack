<template>
	<div>
		<p>子组件</p>
		<p>我是父级传递过来的{{nu}}</p>
		<input type="text" v-model="hh">
		<button @click="sendMsg">传递</button>
	</div>
</template>
<script>
	export default{
		data(){
			return{
				msg:'我是子组件的数据',
				hh:''
			}
		},
		methods:{
			sendMsg(ev){
				//两个参数: 参数1:key  参数2:数据
				this.$emit("sendmsg",this.addNum())
			},
			addNum(){
				return this.nu*this.hh
			}
		},
		props:{
			nu:{
				type:Number,
				default:5
			}
		},
		computed:{
			
		}
	}
</script>
<style></style>