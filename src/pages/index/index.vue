<template>
  <view class="container">
    <view class="static_header">
      <img src="../../../static/images/header-bg.png" />
      <view class="header_main">
        <view class="title">
          <text>文竹园之家</text>
        </view>
        <view class="register">
          <img src="../../../static/images/register.png" />
        </view>
        <view class="main">
          <view class="theme">
            <img src="../../../static/images/header-main.png"/>
          </view>
          <view class="strategy" @click="handleNavTo('../lx/strategy/home/main')">
            <img src="../../../static/images/strategy.png" />
          </view>
        </view>
      </view>
    </view>
    <view class="static_main">
      <view class="server">
        <view class="server_item" v-for="(item, index) in wxPage.serverData" :key="index" @click="handleNavTo(item.url)">
          <image :src="item.iconPath"></image>
          <text>{{item.text}}</text>
        </view>
      </view>
      <view class="server_window">
        <view class="window_item" @click="handleNavTo('../lx/appoint/home/main')">预约服务</view>
        <view class="window_item">志愿者注册</view>
      </view>
      <view class="card">
        <image class="bg" src="/static/images/积分卡底图1@2x.png"></image>
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
      <view class="new">
        <view class="header">
          <text class="title">社区资讯</text>
          <text class="more">查看更多</text>
        </view>
        <view class="new-item" v-for="(item, index) in news" :key="index">
          <view class="new-img">
            <image :src="item.imgUrl"></image>
          </view>
          <view class="content">
            <view class="title">{{item.title}}</view>
            <view class="detail">{{item.detail}}</view>
          </view>
        </view>
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
            text: '社区服务',
            url: '../lx/server/communitySer/main'
          },
          {
            iconPath: '/static/images/社区资讯icon1@2x.png',
            text: '社区资讯',
            url: '../lx/server/communityNew/main'
          }, 
          {
            iconPath: '/static/images/积分兑换icon@2x.png',
            text: '积分兑换',
            url: '../lx/server/exchangeCre/integral/main'
          },
          {
            iconPath: '/static/images/志愿者招募icon@2x.png',
            text: '志愿者招募',
            url: '../lx/server/volunteer/main'
          },
          {
            iconPath: '/static/images/社区社团@2x.png',
            text: '社区社团',
            url: '../lx/server/communityOri/main'
          }
        ]
      },
      news: [
        {
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          detail: '2019年11月30日下午，在文竹园社区老人大学启动仪式顺利进行'
        },
        {
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          detail: '2019年11月30日下午，在文竹园社区老人大学启动仪式顺利进行'
        },
        {
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          detail: '2019年11月30日下午，在文竹园社区老人大学启动仪式顺利进行'
        },
        {
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          detail: '2019年11月30日下午，在文竹园社区老人大学启动仪式顺利进行'
        }
      ]
    }
  },
  methods: {
    handleNavTo(url) {
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