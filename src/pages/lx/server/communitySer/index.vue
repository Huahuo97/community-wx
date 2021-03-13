<template>
  <view class="container">
    <view class="image">
      <image src="/static/images/主图@2x.png" style="width: 550rpx; height:273rpx"></image>
    </view>
    <view class="main">
      <view class="image">
        <image src="/static/images/Layer7@2x.png" style="width: 114rpx; height: 143rpx"></image>
      </view>
      <view class="item" v-for="(item, index) in itemData" :key="index" @click="handleTo(item.url)">
        {{item.text}}
      </view>
    </view>
  </view>
  
</template>

<script>
export default {
  data() {
    return {
      itemData: [
        {
          text: '莘莘学堂',
          url: './school/main'
        },
        {
          text: '社区书店',
          url: './bookshop/main'
        },
        {
          text: '温度空间',
          url: './room/main'
        },
        {
          text: '亲子乐园',
          url: './fairyland/main'
        },
        {
          text: '老年大学',
          url: './oldschool/main'
        },
        {
          text: '为老服务驿站',
          url: './oldserver/main'
        }
      ]
    }
  },
  methods: {
    handleTo(url) {
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