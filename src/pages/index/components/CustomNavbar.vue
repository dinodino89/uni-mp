<template>
  <view class="navbar" :style="{ paddingTop: safeAreaInsets?.top + 'px' }">
    <!-- logo文字 -->
    <view class="flex items-center h-64 pl-30 pt-20">
      <image class="w-200 h-50" src="@/static/images/logo.png"></image>
      <text class="logo-text">新鲜 · 亲民 · 快捷</text>
    </view>
    <!-- 搜索条 -->
    <view class="search">
      <text class="icon-search">搜索商品</text>
      <text class="icon-scan"></text>
    </view>
  </view>
</template>

<script setup lang="ts">
// 获取屏幕边界到安全区域距离
const { safeAreaInsets } = uni.getSystemInfoSync()
</script>

<style lang="scss" scoped>
/* 自定义导航条 */
.navbar {
  @apply flex flex-col pt-20;
  // background-color: pink;
  background-image: url(@/static/images/navigator_bg.png);
  background-size: cover;

  .logo-text {
    flex: 1;
    line-height: 28rpx;
    color: #fff;
    margin: 2rpx 0 0 20rpx;
    padding-left: 20rpx;
    border-left: 1rpx solid #fff;
    font-size: 26rpx;
  }
  .search {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 10rpx 0 26rpx;
    height: 64rpx;
    margin: 16rpx 20rpx;
    color: #fff;
    font-size: 28rpx;
    border-radius: 32rpx;
    background-color: rgba(255, 255, 255, 0.5);
  }
  .icon-search {
    &::before {
      margin-right: 10rpx;
    }
  }
  .icon-scan {
    font-size: 30rpx;
    padding: 15rpx;
  }
}
</style>
