<template>
	<div>
		<p>父组件</p>
		<child @sendmsg="getMsg" :nu="num"/>
		<p>我是从子组件加工的数据{{info}}</p>
	</div>
</template>
<script>
import child from './child'
	export default{
		data(){
			return{
				info:'',
				num:10
			}
		},
		components:{
			child
		},
		methods:{
			getMsg(data){
				this.info=data
			}
		}
	}
</script>
<style></style>