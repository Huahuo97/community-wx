<template>
  <view class="container">
    <view class="static_header">
      <img src="../../../static/images/header-bg.png" />
      <view class="header_main">
        <view class="title">
          <text>我</text>
        </view>
        <view class="register" @click="handleTo('../lx/mine/setting/main')">
          <img src="../../../static/images/register.png" />
        </view>
        <view class="main">
          <view class="theme">
            <img src="../../../static/images/header-main.png"/>
          </view>
        </view>
      </view>
    </view>
    <view class="static_main">
      <view style="width: 100%; height: 1rpx; padding-top: 54rpx"></view>
      <view class="card">
        <image class="bg" src="/static/images/积分卡底图1@2x.png"></image>
        <view class="run-water" @click="handleToRunWater">积分流水</view>
        <view class="header">
          <image class="logo" src="/static/images/文竹园logo@2x.png"></image>
          <text>文竹园积分卡</text>
        </view>
        <view class="card_id">
          <text class="id">**** **** 4657</text>
          <image class="icon" src="/static/images/biyan--@2x.png" style="width: 24rpx; height: 11rpx;"></image>
          <image class="icon" src="/static/images/fuzhi@2x.png" style="width: 21rpx; height: 21rpx;"></image>
        </view>
        <view class="bottom">
          <view class="jifen">
            <view class="item">
              <text>积分收入</text>
              <text>0</text>
            </view>
            <view class="item">
              <text>积分支出</text>
              <text>0</text>
            </view>
            <view class="item">
              <text>总积分</text>
              <text>0</text>
            </view>
          </view>
          <view class="trans">
            <image src="/static/images/转赠icon@2x.png"></image>
            <text>积分转增</text>
          </view>
        </view>
      </view>
      <view class="options">
        <view class="items" @click="handleTo('../lx/mine/contant/main')">联系我们</view>
        <view class="items">我的预约</view>
        <view class="items" @click="handleTo('../lx/mine/voluteer/main')">志愿者</view>
        <view class="items" @click="handleTo('../lx/mine/changeHistory/main')">兑换记录</view>
        <view class="items" @click="handleTo('../lx/mine/suggest/main')">我的建议</view>
      </view>
    </view>
  </view>
</template>

<script>
export default {
  data () {
    return {
      wxPage: {
        serverData: [
          {
            iconPath: '/static/images/社区服务icon@2x.png',
            text: '社区服务'
          },
          {
            iconPath: '/static/images/社区资讯icon1@2x.png',
            text: '社区资讯'
          }, 
          {
            iconPath: '/static/images/积分兑换icon@2x.png',
            text: '积分兑换'
          },
          {
            iconPath: '/static/images/志愿者招募icon@2x.png',
            text: '志愿者招募'
          },
          {
            iconPath: '/static/images/社区社团@2x.png',
            text: '社区社团'
          }
        ]
      }
    }
  },
  methods: {
    handleToRunWater() {
      wx.navigateTo({
        url: '../lx/server/exchangeCre/runwater/main'
      });
    },
    handleTo(url) {
      wx.navigateTo({
        url
      });
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>