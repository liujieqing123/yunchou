<template>
	<div class="home">
		<Header></Header>
		<Banner></Banner>
		<List></List>
		<Footer></Footer>
	</div>
</template>

<script>
	import Header from '../../commons/Header'
	import Banner from '../../commons/Banner'
	import List from '../../commons/List'
	import Footer from '../../commons/Footer'
	
	export default{
		name:'Home',
		components:{Header,Banner,List,Footer},
		data(){
			return{
				name:'Home'
			}
		}
	}
</script>

<style>
</style>