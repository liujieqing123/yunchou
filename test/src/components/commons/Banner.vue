<template>
	<div class="banner">
		<div class="swiper-container">
			<div class="swiper-wrapper">
				<div class="swiper-slide" v-for="(item,index) in List" :key="index">
					<!--<img :src="item">-->
					<img src="../../images/raw_1516957426.jpeg" />
				</div>
			</div>

			<!-- 如果需要滚动条 -->
			<div class="swiper-scrollbar"></div>
		</div>
	</div>
</template>

<script>
	import Swiper from 'swiper'
	import Vue from 'vue'

	export default {
		name: 'Banner',
		components: {},
		data() {
			return {
				name: 'Banner',
				List: []
			}
		},
		methods: {
			getList() {
				setTimeout(() => {
					this.List = [
						"../../images/raw_1516957426.jpeg",
						"../../images/raw_1516957426.jpeg",
						"../../images/raw_1516957426.jpeg"
					]
					Vue.nextTick(() => {
						new Swiper('.swiper-container', {
							spaceBetween: 30,
							centeredSlides: true,
							autoplay: {
								delay: 2500,
								disableOnInteraction: false,
							},
							pagination: {
								el: '.swiper-pagination',
								clickable: true,
							},
							navigation: {
								nextEl: '.swiper-button-next',
								prevEl: '.swiper-button-prev',
							},
						});
					})
				})
//				console.log(1111111);
			}
		},
		created() {
			this.getList();
//			console.log(1111111);
//			console.log(this.List);
		},
		mounted() {

		}

	}
</script>

<style lang="less" scoped>
	@import url("../../styles/main.less");
	@import url("../../../node_modules/swiper/dist/css/swiper.css");
	.banner {
		
		.swiper-container {
			.swiper-wrapper {
				.w(375);
				.h(200);
				.swiper-slide {
					.w(375);
					.h(200);
					img {
						.w(375);
						.h(200);
					}
				}
			}
		}
	}
</style>