<template>
  <view class="container">
    <view class="center">
      <view class="item" v-for="(item, index) in lists" :key="index">
        <view class="top">
          <view class="name">{{item.name}}</view>
          <view class="time">{{item.time}}</view>
        </view>
        <view class="bottom">
          数量：{{item.count}}
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
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        },
        {
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        },
        {
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        },
        {
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        },
        {
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        },
        {
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        },
        {
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        },
        {
          name: '名称',
          count: 1,
          time: '2019年12月10日 11:30:29'
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>