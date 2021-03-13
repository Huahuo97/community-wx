<template>
  <view class="container">
    <view class="center">
      <view class="organization">
        <view class="item" v-for="(item, index) in lists" :key="index">
          <view class="info">
            <view class="img">
              <image :src="item.imgUrl"></image>
            </view>
            <view class="name">{{item.name}}</view>
          </view>
          <button class="apply" @click="toDetail">申请组团</button>
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
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        },
        {
          name: '社团名称'
        }
      ]
    }
  },
  methods: {
    toDetail() {
      wx.navigateTo({
        url: '../detail/main'
      });
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>