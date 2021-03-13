<template>
  <view class="container">
    <view class="center">
      <view class="info">
        <view class="title">{{post.title}}</view>
        <view class="apply-time">报名时间：{{post.applyTime}}</view>
        <view class="cut-off">截止时间：{{post.cutOff}}</view>
        <view class="apply-count">报名人数：{{post.applyed}}/{{post.count}}</view>
        <view class="server-time">服务时间：{{post.serverTime}}</view>
        <view class="icon">
          <view class="income">
            <image src="/static/images/jifen@2x.png"></image>
            <text>报名获得积分 {{post.applyGet}}</text>
          </view>
          <view class="share">
            <image src="/static/images/fenxiang@2x.png"></image>
            <text>分享岗位</text>
          </view>
        </view>
        <view class="apply">报名</view>
      </view>
      <view class="introduce">
        <view class="title">介绍正文</view>
        <view class="img">
          <image :src="post.introduce.imgUrl"></image>
        </view>
        <view class="annotation">{{post.introduce.annotation}}</view>
        <view class="main-body">{{post.introduce.mainBody}}</view>
      </view>
      <view class="volunteer">
        <view class="title">已报名志愿者</view>
        <view class="item" v-for="(item, index) in post.volunteers" :key="index">
          <image :src="item.picture"></image>
          <view class="middle">
            <view class="name">{{item.username}}</view>
            <view class="time">{{item.applyTime}}</view>
          </view>
          <view class="right">
            <view class="state">{{item.state}}</view>
            <view class="rank">No.{{item.rank}}</view>
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
      post: {
        title: '书店岗位服务标题',
        applyTime: '2019.08.18',
        cutOff: '2019.09.18',
        applyed: 16,
        count: 80,
        serverTime: '2019.12.08',
        applyGet: 10,
        introduce: {
          annotation: '图片注释',
          mainBody: '介绍正文'
        },
        volunteers: [
          {
            picture: '/static/images/头像@2x.png',
            username: '周小鱼',
            applyTime: '2019-09-17 12:57:40',
            state: '报名成功',
            rank: 1
          },
          {
            picture: '/static/images/头像@2x.png',
            username: '周小鱼',
            applyTime: '2019-09-17 12:57:40',
            state: '报名成功',
            rank: 1
          },
          {
            picture: '/static/images/头像@2x.png',
            username: '周小鱼',
            applyTime: '2019-09-17 12:57:40',
            state: '报名成功',
            rank: 1
          },
          {
            picture: '/static/images/头像@2x.png',
            username: '周小鱼',
            applyTime: '2019-09-17 12:57:40',
            state: '报名成功',
            rank: 1
          }
        ]
      }
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>