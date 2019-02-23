<template>
	<div>
		<p>ss</p>
		<div><button @click="changView">切换组件</button></div>
		<!-- <keep-alive> -->
			<component :is="currentView"></component>
		<!-- </keep-alive> -->
	</div>
</template>
<script>
import Small1 from './small1'
import Small2 from './small2'
	export default{
		name:"big",
		data(){
			return{
				currentView:'Small1',
				falg:true
			}
		},
		components:{
			Small1,
			Small2
		},
		methods:{
			changView(){
				if(this.falg){
					this.currentView='Small2'
				}else{
					this.currentView='Small1'
				}
				this.falg=!this.falg;
			}
		}
	}
</script>
<style>
	
</style>