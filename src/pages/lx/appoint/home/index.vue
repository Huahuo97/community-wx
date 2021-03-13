<template>
  <view class="container">
    <view class="header">
      <image src="/static/images/背景树@2x.png" style="width: 666rpx; height: 370rpx"></image>
      <image class="person" src="/static/images/Layer1@2x_61.png" style="width: 215rpx; height: 177rpx"></image>
    </view>
    <view class="content">
      <view class="center">
        <view class="item" v-for="(item, index) in servers" :key="index">
          <view class="left">{{item.name}}</view>
          <view class="right">
            <view class="appoint"><button>预约</button></view>
            <view class="get">{{item.get}}积分</view>
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
      servers: [
        {
          name: '为老服务驿站',
          get: 0
        },
        {
          name: '亲子乐园服务',
          get: 0
        },
        {
          name: '午间课堂服务',
          get: 0
        },
        {
          name: '晚间课堂服务',
          get: 200
        },
        {
          name: '四点半课堂服务',
          get: 200
        },
        {
          name: 'VR课堂服务',
          get: 200
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>