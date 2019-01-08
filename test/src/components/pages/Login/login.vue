<template>
	<div class="login">
		<Header></Header>
		<Footer></Footer>
	</div>
</template>

<script>
	import Header from '../../commons/Header'
	import Footer from '../../commons/Footer'
	
	export default{
		name:'Login',
		components:{Header,Footer},
		data(){
			return{
				name:'Login'
			}
		}
	}
</script>
    
<style>

</style>