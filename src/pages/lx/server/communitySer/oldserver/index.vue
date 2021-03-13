<template>
  <view class="container">
    <view class="image">
      <image src="/static/images/主图@2x.png" style="width: 550rpx; height:273rpx"></image>
    </view>
    <view class="main">
      <view class="main-image">
        <image src="/static/images/Layer3@2x.png" style="width: 229rpx; height: 180rpx"></image>
      </view>
      <view class="item" v-for="(item, index) in itemData" :key="index">
        {{item.text}}
        <view class="apply">预约</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      itemData: [
        {
          text: '老人助餐'
        },
        {
          text: '老人助浴'
        },
        {
          text: '老人助行'
        },
        {
          text: '老人助医助护'
        },
        {
          text: '老人助乐助餐'
        },
        {
          text: '老人助办服务'
        }
      ]
    }
  },
}
</script>

<style lang="less">
  @import './index.less';
</style>