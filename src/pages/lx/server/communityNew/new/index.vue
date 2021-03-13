<template>
  <view class="container">
    <view class="banner">
      <swiper indicator-dots autoplay>
        <swiper-item v-for="(item, index) in bannerData" :key="index">
          <image style="width: 750rpx; height: 331rpx" :src="item.imgUrl"></image>
        </swiper-item>
      </swiper>
    </view>
    <view class="new-list">
      <view class="header">资讯列表</view>
      <view class="new-item" v-for="(item, index) in news" :key="index">
        <view class="left">
          <text class="date">{{item.time.date}}</text>
          <text class="year-mon">{{item.time.year}}.{{item.time.month}}</text>
        </view>
        <view class="right">
          <view class="title">{{item.title}}</view>
          <view class="content">{{item.content}}</view>
        </view>
      </view>
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
      news: [
        {
          time: {
            year: 2019,
            month: 10,
            date: 29
          },
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          content: '2019年11月30日下午，在文竹园社区老年大学服务中心举办老人大学启动仪式2019年11月30日下午，在文竹园社区老年大学服务中心，举办老人大学启动仪式'
        },
        {
          time: {
            year: 2019,
            month: 10,
            date: 29
          },
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          content: '2019年11月30日下午，在文竹园社区老年大学服务中心举办老人大学启动仪式2019年11月30日下午，在文竹园社区老年大学服务中心，举办老人大学启动仪式'
        },
        {
          time: {
            year: 2019,
            month: 10,
            date: 29
          },
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          content: '2019年11月30日下午，在文竹园社区老年大学服务中心举办老人大学启动仪式2019年11月30日下午，在文竹园社区老年大学服务中心，举办老人大学启动仪式'
        },
        {
          time: {
            year: 2019,
            month: 10,
            date: 29
          },
          title: '社区助老敬老活动取得圆满成功,社区老人大学启动仪式顺利进行',
          content: '2019年11月30日下午，在文竹园社区老年大学服务中心举办老人大学启动仪式2019年11月30日下午，在文竹园社区老年大学服务中心，举办老人大学启动仪式'
        }
      ]
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>