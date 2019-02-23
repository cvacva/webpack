<template>
	<div>
		<p :class="{active:abc,'demo':'abb'}">我是添加CLASS方法一</p>
		<p :class="styleObject">我是添加CLASS方法二</p>
		<ul>
			<!-- 第三种class添加方法 -->
			<li v-for="item,index in arr" :class="[{a:index%2==0},'info']">{{item}}</li>
		</ul>
	</div>
</template>
<script>
	export default{
		data(){
			return{
				//方法一
				abc:true,
				abb:true,
				//方法二 一般用于这种
				styleObject:{
					sss:true,
					xxx:true
				},
				arr:['士大夫','送给我','的身份过得挺好','让他好吧','而后被']
			}
		}
	}
</script>
<style>
	.active{
		color:red;
	}
	.demo{
		font-size:20px;
	}
	.sss{
		color:green;
	}
	.xxx{
		font-size:26px;
		font-weight:bold;
	}
	.a{background-color:#f1f1f1;}
</style>