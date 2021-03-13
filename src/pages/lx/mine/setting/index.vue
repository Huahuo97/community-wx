<template>
  <view class="container">
    <view class="center">
      <view class="image">
        <image src="/static/images/头像@2x.png"></image>
        <text @click="showPopup">修改头像</text>
      </view>
      <view class="set-item" @click="handleChange('name')">
        <view class="left">姓名</view>
        <view class="right">{{user.name}}</view>
      </view>
      <view class="set-item" @click="handleChange('tel')">
        <view class="left">电话</view>
        <view class="right">{{user.tel}}</view>
      </view>
      <view class="set-item" @click="handleChange('address')">
        <view class="left">地址</view>
        <view class="right">{{user.address}}</view>
      </view>
    </view>
    <van-popup
      :show="show"
      round
      position="bottom"
      custom-style="height: 40%"
    >
      <view class="pop-content">
        <view class="shoot">
          <image src="/static/images/paizhao@2x.png"></image>
          <text>拍照</text>
        </view>
        <view class="photos">
          <image src="/static/images/ziyuan@2x.png"></image>
          <text>相册</text>
        </view>
        <view class="cancle" @click="onClose">取消</view>
      </view>
    </van-popup>
  </view>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: '周小鱼',
        tel: '15819980876'
      },
      show: false
    }
  },
  methods: {
    handleChange(type){
      wx.navigateTo({
        url: `./detail/main?type=${type}`
      })
    },
    showPopup() {
      this.show = true;
    },
    onClose() {
      this.show = false;
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>