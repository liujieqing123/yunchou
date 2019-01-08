<template>
	<div class="footer">
		<div class="content">
			<i class="fa fa-angle-left"></i>
			<i class="fa fa-angle-right"></i>
			<i class="fa fa-bookmark-o"></i>
			<i class="fa fa-book"></i>
			<i class="fa fa-window-restore"></i>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Footer',
		components: {},
		data() {
			return {
				name: 'Footer'
			}
		}
	}
</script>

<style lang="less" scoped>
	@import '../../styles/main.less';
	.footer {
		.content {
			.w(375);
			.h(40);
			background: #eee;
			font-size: 0;
			display: flex;
			justify-content: space-around;
			align-items: center;
			i {
				display: inline-block;
				.w(30);
				.h(30);
				.lh(30);
				text-align: center;
				/*background: red;*/
				.fs(18);
				color: #fff;
			}
		}
	}
</style>