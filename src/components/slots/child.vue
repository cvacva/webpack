<template>
	<div>
		<p>子组件</p>
		<slot name="n1"></slot>
		<hr>
		<slot tex="{msg}" name="n2"></slot>
	</div>
</template>
<script>
	export default{
		data(){
			return{
				msg:'我是子组件的数据',

			}
		}
	}
</script>
<style></style>