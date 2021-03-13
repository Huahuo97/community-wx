<template>
  <view class="container">
    <view class="center">
      <view class="card">
        <image class="bg" src="/static/images/积分卡底图1@2x.png"></image>
        <view class="up">
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
            <view class="trans" @click="handleNavTo('../lx/server/exchangeCre/turn/main')">
              <image src="/static/images/转赠icon@2x.png"></image>
              <text>积分转增</text>
            </view>
        </view>
        </view>
      </view>
      <view class="tags">
        <view class="tag" :style="checked == 'run' ? 'background-color: #69acf4; color: #fff;' : ''" @click="handleCheckTag" data-key="0">积分流水</view>
        <view class="tag" :style="checked == 'income' ? 'background-color: #69acf4; color: #fff;' : ''" @click="handleCheckTag" data-key="1">收入</view>
        <view class="tag" :style="checked == 'pay' ? 'background-color: #69acf4; color: #fff;' : ''" @click="handleCheckTag" data-key="2">支出</view>
      </view>
      <view class="tags-content">
        <view class="item" v-for="(item, index) in tagsContent" :key="index">
          <view class="top">
            <view class="time">{{item.time}}</view>
          </view>
          <view class="bottom">
            <view class="name">{{item.name}}</view>
            <view class="score">{{item.score}}积分</view>
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
      checked: 'run',
      tagsContent: [
        {
          time: '2019年12月10日',
          name: '书店活动',
          score: 200
        },
        {
          time: '2019年12月10日',
          name: '书店活动',
          score: 200
        },
        {
          time: '2019年12月10日',
          name: '书店活动',
          score: 200
        },
        {
          time: '2019年12月10日',
          name: '书店活动',
          score: 200
        },
        {
          time: '2019年12月10日',
          name: '书店活动',
          score: 200
        },
        {
          time: '2019年12月10日',
          name: '书店活动',
          score: 200
        }
      ]
    }
  },
  methods: {
    handleCheckTag(e) {
      const key = e.currentTarget.dataset.key;
      console.log(e);
      console.log(key);
      if (key == 0) {
        this.checked = 'run';
      } else if(key == 1) {
        this.checked = 'income';
      } else {
        this.checked = 'pay';
      }
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>