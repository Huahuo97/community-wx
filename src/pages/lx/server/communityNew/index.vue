<template>
  <view class="container">
    <view class="view">
      <view class="background">
        <image src="/static/images/主图@2x.png" style="width: 607rpx; height: 289rpx"></image>
      </view>
      <view class="plate">
        <view class="plate-item" @click="handleTo">社区资讯</view>
        <view class="plate-item">社区活动</view>
        <view class="plate-item">办事指南</view>
        <view class="plate-item">社区地图</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  methods: {
    handleTo() {
      wx.navigateTo({
        url: './new/main'
      })
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>