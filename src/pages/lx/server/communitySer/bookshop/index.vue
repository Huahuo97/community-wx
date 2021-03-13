<template>
  <view class="container">
    <view class="banner">
      <swiper indicator-dots autoplay>
        <swiper-item v-for="(item, index) in bannerData" :key="index">
          <image style="width: 750rpx; height: 331rpx" :src="item.imgUrl"></image>
        </swiper-item>
      </swiper>
    </view>
    <view class="activity">
      <view class="header">书店活动</view>  
      <scroll-view scroll-x="true" class="contain">
        <view class="item" v-for="(item, index) in activityData" :key="index">
          <view class="image">
            <view class="star"></view>
          </view>
          <view class="title">{{item.title}}</view>
          <view class="activity-time">活动时间：{{item.time}}</view>
          <view class="new">资讯简介</view> 
        </view>
      </scroll-view>  
    </view>
    <view class="song-bird">
      <view class="header">
        <view class="logo">
          <image src="/static/images/song-bird.png" style="width: 70rpx; height: 103rpx"></image>
        </view>
        <view class="contain">
          <view class="bg">青鸟想读</view>  
          <view class="xs">每一本都是你想读的书</view>  
        </view>
        <view class="button">
          查看心愿
        </view>
      </view>
      <view class="bottom">
        <view class="bottom-item">
          <view class="title">青鸟智造</view>
          <view class="info">和书友一起制作文创产品</view>
        </view>
        <view class="bottom-item">
          <view class="title">青鸟还书</view>
          <view class="info">还书并发布读后感</view>
        </view>
      </view>
      <view class="apply-button">发布书籍心愿，免费借阅</view>
    </view>
    <view class="want-to">
      <view class="title">精品想读</view>
      <view class="contain">
        <scroll-view scroll-x="true" class="main">
          <view class="item" v-for="(item, index1) in wantToData" :key="index1">
            <view class="image">
              <view class="help">想帮</view>
              <view class="read">
                <image src="/static/images/shoucang@2x.png"></image>
              </view>
            </view>
            <view class="icon">
              <view class="icon-item" v-for="index2 of item.count" :key="index2">
                <image src="/static/images/user-icon.png"></image>
              </view>
            </view>
            <view class="done">
              已有{{item.count}}人想读
            </view>
          </view>
        </scroll-view>
      </view>
    </view>
    <view class="want-to">
      <view class="title">想读心愿</view>
      <view class="contain">
        <scroll-view scroll-x="true" class="main">
          <view class="item" v-for="(item, index1) in wantToData" :key="index1">
            <view class="image">
              <view class="help">想帮</view>
              <view class="read">
                <image src="/static/images/shoucang@2x.png"></image>
              </view>
            </view>
            <view class="icon">
              <view class="icon-item" v-for="index2 of item.count" :key="index2">
                <image src="/static/images/user-icon.png"></image>
              </view>
            </view>
            <view class="done">
              已有{{item.count}}人想读
            </view>
          </view>
        </scroll-view>
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
      activityData: [
        {
          title: '画展',
          time: '2019年10月21日18:00-21:00'
        },
        {
          title: '读书会',
          time: '2019年10月21日18:00-21:00'
        },
        {
          title: '相声会',
          time: '2019年10月21日18:00-21:00'
        }
      ],
      wantToData: [
        {
          count: 5
        },
        {
          count: 4
        },
        {
          count: 2
        },
        {
          count: 1
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>