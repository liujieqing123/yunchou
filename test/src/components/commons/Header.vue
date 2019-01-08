<template>
	<div class="header">
		<div class="title">
			<div class="title-top">
				<div class="t-left">
					<img src="../../images/raw_1517815359.png" />
					<span>运筹</span>
				</div>
				<i class="fa fa-list" @click="toggle()"></i>
			</div>
			<ul>
				 <li @click="seleItem(item)" :class="sel==item?'hl':''" v-for="(item,index) in list" :key="index"><a>{{item}}</a></li>
			</ul>
		</div>
		<Nav :show='isShow'></Nav>
	</div>
</template>

<script>
	import Nav from './Nav'
	export default {
		name: 'Header',
		components: {Nav},
		data() {
			return {
				name: 'Header',
				list:[],
				sel: '全部',
				isShow:false
			}
		},
		methods:{
				navList(){
					setTimeout(()=>{
						this.list=["全部","筹集中","未开始","已结束"]						
					})
				},
				seleItem(item){
					this.sel=item;
				},
				toggle(){
				this.isShow=!this.isShow
			}
		},
		created() {
			this.navList();
		}
		
	}
</script>

<style lang="less" scoped>
	@import '../../styles/main.less';
	.header {
		/*position:relative;*/
		.title {
			.w(375);
			.h(90);
			background: #62707F;
			.title-top {
				.w(375);
				.h(45);
				.lh(45);
				.padding(5,20,5,10);
				color:#fff;
				display: flex;
				justify-content: space-between;
				align-items: center;
				/*font-size:0px;*/
				.fs(14);
				.t-left {
					img {
						.w(30);
						.h(30);
					}
				}
				i {
					display:inline-block;
					.w(24);
					.h(24);
					.fs(24);
				}
			}
			ul{
				.w(375);
				.h(50);
				display: flex;
				justify-content: space-around;
				align-items: center;
				li{
					.h(23);
					.fs(14);
					color:#fff;
					float:left;
					a{
					  display:inline-block;
					  /*.w(40);*/
					  .h(30);
					}
				}
				.hl{
					a{
						border-bottom:2px solid orange;
					}
				}
			}
		}
	}
</style>