<template>
	<div class="login">
		<!-- 头部 -->
		<van-nav-bar placehokder title="淘客" right-text="登录" @click-left="onClickLeft" @click-right="onClickRight" />
		<!-- input 搜索框 -->
		<van-search background="#4fc08d" v-model="value" placeholder="请输入搜索关键词" />
		<!-- 轮播图 -->
		<van-swipe class="my-swipe" :autoplay="3000" indicator-color="white">
			<van-swipe-item>1</van-swipe-item>
			<van-swipe-item>2</van-swipe-item>
			<van-swipe-item>3</van-swipe-item>
			<van-swipe-item>4</van-swipe-item>
			<van-swipe-item>5</van-swipe-item>
			<!-- <van-swipe-item v-for="(image, index) in images" :key="index">
				<img v-lazy="image" />
			</van-swipe-item> -->
		</van-swipe>
		<!-- 宫格 -->
		<van-grid :column-num="5">
			<!-- <van-grid-item icon="photo-o" text="分类" /> -->
			<van-grid-item v-for="value in 10" :key="value" icon="photo-o" text="文字" />
		</van-grid>
		<!-- 活动 -->
		<div class="activity">
			<!-- 骨架屏  内容-->
			<van-skeleton title :row="20" />
		</div>
		<!-- 链接 -->
		<div class="link">
			链接
		</div>
		<!-- 底部 -->
		<van-tabbar v-model="active" placeholder>
			<van-tabbar-item icon="home-o">首页</van-tabbar-item>
			<van-tabbar-item icon="search">标签</van-tabbar-item>
			<van-tabbar-item icon="friends-o">标签</van-tabbar-item>
			<van-tabbar-item icon="setting-o">标签</van-tabbar-item>
		</van-tabbar>
	</div>
</template>
<script>
	export default {
	name: 'login',
	data() {
		return {
			value: '',
			active: 0,
			images: [
        'https://img.yzcdn.cn/vant/apple-1.jpg',
        'https://img.yzcdn.cn/vant/apple-2.jpg',
      ],
		};
	},
	methods: {
    onClickLeft() {
      Toast('返回');
    },
    onClickRight() {
      Toast('按钮');
    },
  },

}

</script>
<style type="text/css">
.top {
	height: 40px;
	background-color: #f55;
}

.my-swipe .van-swipe-item {
	color: #fff;
	font-size: 20px;
	line-height: 150px;
	text-align: center;
	background-color: #39a9ed;
}

/*商品*/
.commodity {
	height: 100px;
	background-color: #66f;
}

/*链接*/
.link {
	height: 100px;
	background-color: #f6f;
}

</style>
