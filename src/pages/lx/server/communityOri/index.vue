<template>
  <view class="container">
    <view class="center">
      <view class="banner">
        <swiper indicator-dots="true" autoplay="true" interval="2000" duration="500">
          <swiper-item v-for="(item, index) in bannerData" :key="index">
            <image style="width: 686rpx; height: 331rpx" :src="item.imgUrl"></image>
          </swiper-item>
        </swiper>
      </view>
      <view class="type">
        <view class="item" @click="toActivity">
          <image src="/static/images/renyuan-3@2x.png"></image>
          <text>社团活动</text>
        </view>
        <view class="item">
          <image src="/static/images/申请组团icon@2x.png"></image>
          <text>申请组团</text>
        </view>
      </view>
      <view class="organization">
        <view class="title">社区社团<text class="more" @click="toMore">查看更多</text></view>
        <view class="content">
          <view class="item" v-for="(item, index) in organs" :key="index" @click="toDetail">
            <view class="img">
              <image src="item.imgUrl"></image>
            </view>
            <view class="name">
              {{item.name}}
            </view>
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
      bannerData: [
        {
          imgUrl: '/static/images/Rectangle13copy2@2x.png'
        },
        {
          imgUrl: '/static/images/Rectangle13copy2@2x.png'
        },
        {
          imgUrl: '/static/images/Rectangle13copy2@2x.png'
        },
        {
          imgUrl: '/static/images/Rectangle13copy2@2x.png'
        },
        {
          imgUrl: '/static/images/Rectangle13copy2@2x.png'
        }
      ],
      organs: [
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        }
      ]
    }
  },
  methods: {
    toActivity() {
      wx.navigateTo({
        url: './activity/main'
      });
    },
    toMore() {
      wx.navigateTo({
        url: './organization/main'
      });
    },
    toDetail() {
      wx.navigateTo({
        url: './detail/main'
      });
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>