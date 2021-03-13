<template>
  <view class="container">
    <view class="center">
      <view class="info">
        <view class="card">
          <image class="backgroung" src="/static/images/文竹园社区志愿者信息卡@2x.png" style="width: 644rpx; height: 308rpx"></image>
          <view class="data-bank">
            <view class="name">姓名：{{mine.name}}</view>
            <view class="tel">电话：{{mine.tel}}</view>
            <view class="id">编号：{{mine.id}}</view>
          </view>
          <view class="erweima">
            <image :src="mine.erweimaImg"></image>
          </view>
          <view class="change" @click="handleTo('../voluteerSetting/main')">修改信息</view>
        </view>
        <view class="tags">
          <view class="left" @click="handleCheck" data-key="0" :style="checked == 'applyed' ? 'color: #333232' : ''">志愿者报名信息</view>
          <view class="right" @click="handleCheck" data-key="1" :style="checked == 'history' ? 'color: #333232' : ''">志愿服务记录</view>
        </view>
        <view class="asset">
          <view class="item">
            <view class="left">
              <image src="/static/images/jifen.png"></image>
              <text>总积分</text>
            </view>
            <view class="right">
              <text>{{mine.asset.integral}}</text>积分
            </view>
          </view>
          <view class="item">
            <view class="left">
              <image src="/static/images/shijian@2x.png"></image>
              <text>服务时间</text>
            </view>
            <view class="right">
              <text>{{mine.asset.time}}</text>小时
            </view>
          </view>
        </view>
      </view>
      <view class="content">
        <view class="applyed" v-if="checked == 'applyed'">
          <view class="item" v-for="(item1, index1) in mine.applyed" :key="index1">
            <view class="post">岗位：{{item1.post}}</view>
            <view class="name">姓名：{{item1.name}}</view>
            <view class="tel">电话：{{item1.tel}}</view>
            <view class="time">服务时间：{{item1.time}}</view>
            <button class="sign-in">签到</button>
            <button class="cancel">取消报名</button>
          </view>
        </view>
        <view class="history" v-if="checked == 'history'">
          <view class="title">志愿服务记录</view>
          <view class="item" v-for="(item, index) in mine.history" :key="index">
            <view class="left">
              <image :src="item.imgUrl"></image>
            </view>
            <view class="middle">
              <view class="name">{{item.name}}</view>
              <view class="time">{{item.time}}</view>
            </view>
            <view class="right">
              <text>{{item.makeout}}</text> 积分
            </view>
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
      mine: {
        name: '周鱼',
        tel: '15833920987',
        id: '1793201012350',
        erweimaImg: '/static/images/erweima@2x.png',
        asset: {
          integral: 2000,
          time: 300
        },
        history: [
          {
            name: '书店志愿服务',
            time: '2019年10月21日 18:00-21:00',
            makeout: 5
          },
          {
            name: '温度空间志愿服务',
            time: '2019年10月21日 18:00-21:00',
            makeout: 20
          },
          {
            name: '学堂志愿服务',
            time: '2019年10月21日 18:00-21:00',
            makeout: 200
          },
          {
            name: '书店志愿服务',
            time: '2019年10月21日 18:00-21:00',
            makeout: 100
          },
          {
            name: '书店活动服务',
            time: '2019年10月21日 18:00-21:00',
            makeout: 200
          },
          {
            name: '咖啡厅岗位服务',
            time: '2019年10月21日 18:00-21:00',
            makeout: 200
          } 
        ],
        applyed: [
          {
            post: '书店志愿服务',
            name: '周鱼',
            tel: '18566789978',
            time: '2019年10月21日 18:00-21:00'
          },
          {
            post: '书店志愿服务',
            name: '周鱼',
            tel: '18566789978',
            time: '2019年10月21日 18:00-21:00'
          },
          {
            post: '书店志愿服务',
            name: '周鱼',
            tel: '18566789978',
            time: '2019年10月21日 18:00-21:00'
          },
          {
            post: '书店志愿服务',
            name: '周鱼',
            tel: '18566789978',
            time: '2019年10月21日 18:00-21:00'
          },
          {
            post: '书店志愿服务',
            name: '周鱼',
            tel: '18566789978',
            time: '2019年10月21日 18:00-21:00'
          },
          {
            post: '书店志愿服务',
            name: '周鱼',
            tel: '18566789978',
            time: '2019年10月21日 18:00-21:00'
          }
        ]
      },
      checked: 'applyed'
    }
  },
  methods: {
    handleTo(url) {
      wx.navigateTo({
        url
      });
    },
    handleCheck(e) {
      const key = e.currentTarget.dataset.key;
      if(key == 0) {
        this.checked = 'applyed';
      } else {
        this.checked = 'history';
      }
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>