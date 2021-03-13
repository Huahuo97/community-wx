<template>
  <view class="container">
    <view class="center">
      <view class="set-item">
        <view class="left">姓名</view>
        <view class="right">{{user.name}}</view>
      </view>
      <view class="set-item">
        <view class="left">电话</view>
        <view class="right">{{user.tel}}</view>
      </view>
      <view class="set-item">
        <view class="left">地址</view>
        <view class="right">{{user.address}}</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: '周小鱼',
        tel: '15819980876'
      }
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>