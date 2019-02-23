<template>
	<div>
		父级
		<son title="传递数据"/>
	</div>
</template>
<script>
	import son from './son'
	export default{
		data(){
			return{
				
			}
		},
		components:{
			son
		}
	}
</script>
<style>
	
</style>