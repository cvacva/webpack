<template>
	<div>
		<p>父组件</p>
		<Child>
			<p slot="n1">我是插槽1</p>
			<p slot="n2" slot-scope="props" >{{props.tex}}</p>
		</Child>
	</div>
</template>
<script>
import Child from './child'
	export default{
		data(){
			return{

			}
		},
		components:{
			Child
		}
	}
</script>
<style></style>