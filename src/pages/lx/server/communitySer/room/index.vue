<template>
  <view class="container">
    <view class="banner">
      <view class="banner">
        <swiper indicator-dots autoplay>
          <swiper-item v-for="(item, index) in bannerData" :key="index">
            <image style="width: 750rpx; height: 331rpx" :src="item.imgUrl"></image>
          </swiper-item>
        </swiper>
      </view>
    </view>
    <view class="order">
      <view class="header">西点点餐</view>
      <view class="contain">
        <scroll-view scroll-x="true" class="items">
          <view class="order-item" v-for="(item, index) in orderData" :key="index">
            <view class="image"></view>
            <view class="name">{{item.name}}</view>
            <view class="pay">消耗积分：{{item.pay}}</view>
            <view class="add" @click="handleChoose(item)">+</view>
          </view>
        </scroll-view>
      </view>
    </view>
    <view class="order-nowest">
      <view class="header">点餐</view>
      <view class="contain">
        <view class="item" v-for="(item, index1) in order1Data" :key="index1">
          <view class="image"></view>
          <view class="main">
            <view class="name">{{item.name}}</view>
            <view class="pay">消耗积分：{{item.pay}}</view>
          </view>
          <view class="add" @click="handleChoose(item)">+</view>
        </view>
      </view>
    </view>
    <van-popup
      :show="show"
      round
      position="bottom"
      closeable
      close-icon="/static/images/delete@2x.png"
      custom-style="height: 40%"
      @close="Onclose"
      close-on-click-overlay
    >
      <view class="middle">
        <view class="title">已选餐饮</view>
        <view class="card-has" v-for="(hasitem, indexHas) in hasChoose" :key="indexHas">
          <view class="left">
            <image></image>
          </view>
          <view class="middle">
            <view class="named">{{hasitem.name}}</view>
            <view class="need-pay">消费积分：{{hasitem.pay}}</view>
          </view>
          <view class="right">
            <view class="dec"><button>-</button></view>
            <view class="count">1</view>
            <view class="add"><button>+</button></view>
          </view>
        </view>
      </view>
    </van-popup>
    <view class="pay">
      <view class="shopcar" @click="Onshow">
        <view class="image">
          <view class="count">{{hasCount | 0}}</view>
        </view>
      </view>
      <view class="has-goods">
        已选餐饮 <text>{{hasPay | 0}}</text>积分
      </view>
      <view class="pay-button">去结算</view>
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
      orderData: [
        {
          name: '餐饮名称',
          pay: 200
        },
        {
          name: '餐饮名称',
          pay: 200
        },
        {
          name: '餐饮名称',
          pay: 200
        }
      ],
      order1Data: [
        {
          name: '餐饮名称',
          pay: 200
        },
        {
          name: '餐饮名称',
          pay: 200
        },
        {
          name: '餐饮名称',
          pay: 200
        }
      ],
      hasChoose: [],
      show: false,
      hasCount: 0
    }
  },
  methods: {
    Onclose() {
      this.show = false;
    },
    Onshow() {
      this.show = true;
    },
    handleChoose(item) {
      this.hasChoose = this.hasChoose.concat(item);
      this.hasCount = this.hasChoose.length;
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>