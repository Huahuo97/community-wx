<template>
  <view class="container">
    <!-- 轮播图 -->
    <view class="banner">
      <swiper indicator-dots="true" autoplay="true" interval="2000" duration="500">
        <swiper-item v-for="(item, index) in bannerData" :key="index">
          <image style="width: 750rpx; height: 331rpx" :src="item.imgUrl"></image>
        </swiper-item>
      </swiper>
    </view>
    <!-- 活动预告 -->
    <view class="foreshow">
      <view class="header">活动预告</view>  
      <scroll-view scroll-x="true" class="contain">
        <view class="item" v-for="(item, index) in foreshowData" :key="index">
          <image :src="item.imgUrl"></image>
          <view class="title">{{item.title}}</view>
        </view>
      </scroll-view>  
    </view>
    <view class="lists">
      <view class="header">活动列表</view>
      <view class="contain">
        <view class="item" v-for="(item, index) in listsData" :key="index">
          <image :src="item.imgUrl"></image>
          <view class="main">
            <view class="title">{{item.title}}</view>
            <view class="count">报名人数：{{item.applyCount}}</view>
            <view class="activity-time">活动时间：{{item.activityTime}}</view>
            <view class="apply-time">报名时间：{{item.applyTime}}</view>
          </view>
          <view class="apply">
            报名
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
      foreshowData: [
        {
          imgUrl: '/static/images/Rectangle@2x.png',
          title: '亲子乐园射击培训活动'
        },
        {
          imgUrl: '/static/images/Rectangle@2x.png',
          title: '亲子乐园射击培训活动'
        },
        {
          imgUrl: '/static/images/Rectangle@2x.png',
          title: '亲子乐园射击培训活动'
        }
      ],
      listsData: [
        {
          imgUrl: '/static/images/Rectangle7@2x.png',
          title: '亲子乐园射击培训活动',
          applyCount: '2/20',
          activityTime: '2019年10月21日18:00-20:00',
          applyTime: '2019年10月6日截止预约'
        },
        {
          imgUrl: '/static/images/Rectangle7@2x.png',
          title: '亲子乐园射击培训活动',
          applyCount: '2/20',
          activityTime: '2019年10月21日18:00-20:00',
          applyTime: '2019年10月6日截止预约'
        },
        {
          imgUrl: '/static/images/Rectangle7@2x.png',
          title: '亲子乐园射击培训活动',
          applyCount: '2/20',
          activityTime: '2019年10月21日18:00-20:00',
          applyTime: '2019年10月6日截止预约'
        },
        {
          imgUrl: '/static/images/Rectangle7@2x.png',
          title: '亲子乐园射击培训活动',
          applyCount: '2/20',
          activityTime: '2019年10月21日18:00-20:00',
          applyTime: '2019年10月6日截止预约'
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>