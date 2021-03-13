<template>
  <view class="container">
    <view class="center">
      <view class="activities" v-for="(item, index) in lists" :key="index">
        <view class="img">
          <image :src="item.imgUrl"></image>
          <view class="title">{{item.title}}</view>
        </view>
        <view class="bottom">
          <view class="applyed">报名人数：{{item.applyed}}/{{item.count}}</view>
          <view class="activity-time">活动时间：{{item.activityTime}}</view>
          <view class="apply-time">报名时间：{{item.applyTime}}</view>
          <view class="apply">
            <button>报名</button>
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
      lists: [
        {
          title: '社区活动标题',
          applyed: 2,
          count: 20,
          activityTime: '2019年10月21日 18:00-20:00',
          applyTime: '2019年10月6日'
        },
        {
          title: '社区活动标题',
          applyed: 2,
          count: 20,
          activityTime: '2019年10月21日 18:00-20:00',
          applyTime: '2019年10月6日'
        },
        {
          title: '社区活动标题',
          applyed: 2,
          count: 20,
          activityTime: '2019年10月21日 18:00-20:00',
          applyTime: '2019年10月6日'
        },
        {
          title: '社区活动标题',
          applyed: 2,
          count: 20,
          activityTime: '2019年10月21日 18:00-20:00',
          applyTime: '2019年10月6日'
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>