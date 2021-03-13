<template>
  <view class="container">
    <view class="header">
      <view class="bg">
        <image src="/static/images/主图@2x.png" style="width:505rpx; height: 273rpx"></image>
      </view>
      <view class="register">
        <image class="icon" src="/static/images/Layer1@2x.png"></image>
        <text>志愿者注册</text>
      </view>
      <view class="know">须知</view>
    </view>
    <view class="main">
      <view class="center">
        <view class="lable">
          <view class="item" :style="checked == 1 ? 'color: #90c1a5' : ''" @click="handleCheck" data-key="1">
            <image src="/static/images/yundong@2x.png" style="width: 36rpx; height: 37rpx"></image>
            <text>志愿活动服务</text>
            <view class="border" v-if="checked == 1"></view>
          </view>
          <view class="item" :style="checked == 2 ? 'color: #90c1a5' : ''" @click="handleCheck" data-key="2">
            <image src="/static/images/gangwei@2x.png" style="width: 36rpx; height: 37rpx"></image>
            <text>志愿岗位服务</text>
            <view class="border" v-if="checked == 2"></view>
          </view>
        </view>
        <!-- 志愿活动服务 -->
        <view class="sports" v-if="checked == 1">
          <view class="item"  v-for="(item, index) in sports" :key="index">
            <view class="sport-img">
              <image :src="item.imgUrl"></image>
            </view>
            <view class="info">
              <text class="name">{{item.name}}</text>
              <text class="make">赚积分：{{item.make}}</text>
            </view>
            <view class="apply">报名</view>
          </view>
        </view>
        <!-- 志愿岗位服务 -->
        <view class="posts" v-if="checked == 2">
          <view class="item"  v-for="(item, index) in posts" :key="index">
            <text>{{item.name}}</text>
            <view class="apply" @click="handleToDetail">报名</view>
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
      checked: 1,
      sports: [
        {
          name: '志愿活动服务名称',
          make: 100
        },
        {
          name: '志愿活动服务名称',
          make: 100
        },
        {
          name: '志愿活动服务名称',
          make: 100
        },
        {
          name: '志愿活动服务名称',
          make: 100
        },
        {
          name: '志愿活动服务名称',
          make: 100
        },
        {
          name: '志愿活动服务名称',
          make: 100
        }
      ],
      posts: [
        {
          name: '社区书店'
        },
        {
          name: '亲子乐园'
        },
        {
          name: '午间课堂'
        },
        {
          name: '晚间课堂'
        },
        {
          name: '四点半课堂'
        },
        {
          name: '温度空间'
        },
        {
          name: '咨询台'
        }
      ]
    }
  },
  methods: {
    handleCheck(e) {
      this.checked = e.currentTarget.dataset.key;
    },
    handleToDetail() {
      wx.navigateTo({
        url: './posts/main'
      });
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>