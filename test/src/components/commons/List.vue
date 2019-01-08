<template>
	<div class="list">
		<div class="content">
			<ul>
				<li v-for="item in 5 ">
					<div class="pt">
                         <img src="../../images/raw_1516856938.png" />
					</div>
					<div class="title">
                        <p>EOS</p>
                        <span>好几十块的私底下</span>
					</div>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'List',
		components: {},
		data() {
			return {
				name: 'List'
			}
		}
	}
</script>

<style lang="less" scoped>
	@import url("../../styles/main.less");
	.list {
		.content {
			ul {
				.w(375);
				li {
					.w(340);
					.h(110);
					.margin(15,
					15,
					0,
					15);
					.padding(0,0,0,20);
					border: 1px solid #ccc;
					display: flex;
					justify-content: space-between;
					align-items: center;
					.pt {
						.w(74);
						.h(74);
						border: 1px solid #ccc;
						float: left;
						img{
							.w(74);
						.h(74);
						}
					}
					.title {
						.w(235);
						.h(75);
						/*border: 1px solid blue;*/
						float: left;
						font-size:0;
						p{
							.fs(18);
							color:#0087D1;
							font-weight:700;
							.margin(0,0,10,0);
						}
						span{
							.fs(12);
							color:#ccc;
							
						}
					}
				}
			}
		}
	}
</style>