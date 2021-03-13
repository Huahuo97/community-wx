<template>
  <view class="container">
    <view class="center">
      <view class="detail-image">
        <image :src="detail.imgUrl"></image>
      </view>
      <view class="detail">
        <view class="header">社团名称<button class="apply">申请组团</button></view>
        <!-- 社团详情 -->
        <view class="main"></view>
      </view>
    </view>
  </view>
</template>

<script>
export default {

}
</script>

<style lang="less">
  @import './index.less';
</style>