<template>
  <view class="container">
    <view class="header">
      <view class="mine">
        <view class="icon">
          <image src="/static/images/jifen@2x.png" style="width: 34rpx; height: 34rpx"></image>
          <text>我的积分：{{myIntegral | 0}}</text>
        </view>
      </view>
      <view class="record">兑换记录</view>
      <view class="bg">
        <image src="/static/images/主图@2x.png" style="width: 505rpx; height: 273rpx"></image>
      </view>
    </view>
    <view class="main">
      <view class="center">
        <view class="shop">
          <view class="title">爱心服务超市</view>
          <view class="category">
            <view class="item">
              <image src="/static/images/food-icon.png"></image>
              <text>西点</text>
            </view>
            <view class="item">
              <image src="/static/images/coffee-icon.png"></image>
              <text>咖啡</text>
            </view>
            <view class="item">
              <image src="/static/images/house-icon.png"></image>
              <text>二手商品</text>
            </view>
            <view class="item">
              <image src="/static/images/cloth-icon.png"></image>
              <text>居民捐赠</text>
            </view>
          </view>
        </view>
        <view class="goods">
          <view class="item" v-for="(item, index) in goods" :key="index">
            <view class="good-img">
              <image :src="item.imgUrl"></image>
            </view>
            <view class="info">
              <text class="name">{{item.name}}</text>
              <text class="pay">积分：{{item.pay}}</text>
            </view>
            <view class="exchange">兑换</view>
          </view>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      goods: [
        {
          name: '兑换物品名称',
          pay: 100
        },
        {
          name: '兑换物品名称',
          pay: 100
        },
        {
          name: '兑换物品名称',
          pay: 100
        },
        {
          name: '兑换物品名称',
          pay: 100
        },
        {
          name: '兑换物品名称',
          pay: 100
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>