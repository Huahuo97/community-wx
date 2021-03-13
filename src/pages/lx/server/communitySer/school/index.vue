<template>
  <view class="container">
    <view class="banner">
      <swiper indicator-dots autoplay>
        <swiper-item v-for="(item, index) in bannerData" :key="index">
          <image style="width: 750rpx; height: 331rpx" :src="item.imgUrl"></image>
        </swiper-item>
      </swiper>
    </view>
    <view class="class-items">
      <view class="item" v-for="(item, index) in classItem" :key="index">
        <text>{{item.text}}</text><view class="apply">预约</view>
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
      classItem: [
        {
          text: '午间课堂'
        },
        {
          text: '晚间课堂'
        },
        {
          text: '四点半课堂'
        },
        {
          text: 'VR课堂'
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>