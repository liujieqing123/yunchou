<template>
	<div class="nav">
		
		<ul v-show='show'>
		   <li>
		   	  <i class="fa fa-user-circle"></i>
		   	  <span>注册</span>
		   	  <span>登录</span>
		   </li>
		   <li>
		   	  <span class="sy">首页</span>
		   </li>
		   <li></li>		   
		</ul>
		
		<div class='mask' v-show='show'></div>
		
	</div>
</template>

<script>
	
	export default{
		name:'Nav',
		components:{},
		props:['show'],
		data(){
			return{
				name:'Nav'
			}
		}
	}
</script>

<style lang="less" scoped>
@import url("../../styles/main.less");
   .nav{
   	   ul{
   	   	  .w(250);
   	   	  .h(599);
   	   	  background:#ccc;
   	   	  position: fixed;
   	   	  top:90px;
   	   	  right:0px;
   	   	  z-index:900;
   	   	  li{
   	   	  	.w(250);
   	   	  	.h(50);
   	   	  	.padding(0,0,0,20);
   	   	  	border-bottom:1px solid #fff;
   	   	  	.lh(50);
   	   	  	font-size:0;
   	   	  	i{
   	   	  		display: inline-block;
				.w(30);
				.h(30);
				.fs(20);
   	   	  	}
   	   	  	span{
   	   	  		display: inline-block;
				.w(60);
				.h(30);
				.fs(15);
				.lh(30);
				.margin(0,0,0,10);
				text-align:center;
				background:blue;
   	   	  	}
   	   	  	.sy{
   	   	  		display: inline-block;
				.w(60);
				.h(30);
				.fs(15);
				.lh(30);
				background:none;
   	   	  	}
   	   	  }
   	   }
   	  .mask{
 		position: fixed;
 		.top(90);
 		bottom:0;
 		left:0;
 		right: 0;
 		background: rgba(0,0,0,.4);
 	}
   }
</style>