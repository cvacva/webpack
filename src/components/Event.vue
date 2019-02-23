<template>
	<div class="event">
		<button @click="show">按钮1</button>
		<button>按钮2</button>
		<ul v-show="flag">
			<li>jhsd</li>
			<li>jhsd</li>
			<li>jhsd</li>
		</ul>
		<button v-on:click="shy">按钮3</button>
		<ul>
			<li v-for="item in name">{{item}}</li>
		</ul>
		<div>
			<p>{{msgre}}</p>
			<p>{{meassage.split('').reverse().join('')}}</p>
		</div>
	</div>
</template>
<script>
	export default{
		data(){
			return{
				name:['威廉','赵云','武则天','老夫子'],
				flag:true,
				a:0,
				meassage:'hello Vue !!!'
			}
		},
		methods:{
			show(){
				this.flag=!this.flag;
			},
			shy(){
				this.name.push(this.a++)
			}
		},
		computed:{
			msgre(){
				return this.meassage.split('').reverse().join('');
			}
		}
	}
</script>
<style scoped>
	 @import '../css/mod_1.css'
</style>