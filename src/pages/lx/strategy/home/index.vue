<template>
  <view class="container">
    <view class="header">
      <image src="/static/images/背景树@2x.png" style="width: 666rpx; height: 370rpx"></image>
      <image class="person" src="/static/images/人@2x.png" style="width: 116rpx; height: 175rpx"></image>
    </view>
    <view class="content">
      <view class="center">
        <view v-if="showHelp">
          <view class="help" v-for="(item, index) in helps" :key="index" @click="handleAnswer(item)">
            {{item.question}}
           </view>
        </view>
        <view v-if="!showHelp">
          <view class="answer">
            <view class="title">{{answer.question}}</view>
            <view class="content">{{answer.answer}}</view>
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
      helps: [
        {
          question: '如何获得积分？'
        },
        {
          question: '如何报名午间课堂？'
        },
        {
          question: '如何报名晚间课堂？'
        },
        {
          question: '如何报名四点半课堂？'
        },
        {
          question: '哪些服务项目需要积分？'
        },
        {
          question: '亲子乐园需要积分？'
        },
        {
          question: '如何在小程序上预约老人助餐？'
        }
      ],
      answer: {},
      showHelp: true
    }
  },
  methods: {
    handleAnswer(item) {
      this.showHelp = false;
      this.answer = item;
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>