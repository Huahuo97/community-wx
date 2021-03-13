<template>
  <view class="container">
    <view class="header">
      <image src="/static/images/背景树@2x.png" style="width: 666rpx; height: 370rpx"></image>
      <image class="person" src="/static/images/Layer3@2x_68.png" style="width: 182rpx; height: 192rpx"></image>
    </view>
    <view class="content">
      <view class="center">
        <view class="photo">
          <image v-for="(item, index) in addPhotos" :key="index" :src="item" style="width: 208rpx; height: 104rpx"></image>
          <view class="add">
            <view class="icon">+</view>
            <view class="text">添加图片</view>
          </view>
        </view>
        <view class="apply"><button>发布</button></view>
        <view class="title">
          <input type="text" placeholder="请输入建议标题" v-model="title" />
        </view>
        <view class="suggestion">
          <textarea placeholder="请输入建议内容" v-model="suggestion"></textarea>
        </view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      addPhotos: [],
      title: '',
      suggestion: ''
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>