<template>
  <view class="container">
    <view class="center">
      <view class="tel" v-if="type == 'tel'">
        <view>
          <input placeholder="修改电话" v-model="user.tel"/>
        </view>
        <view class="verify">
          <input placeholder="验证码" v-model="verify"/>
          <view class="send">发送验证码</view>
        </view>
      </view>
      <view class="address" v-if="type == 'address'">
        <view>
          <input placeholder="修改地址" v-model="user.address"/>
        </view>
      </view>
      <view class="name" v-if="type == 'name'">
        <view>
          <input placeholder="修改姓名" v-model="user.name"/>
        </view>
      </view>
      <button class="change">修改</button>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      type: '',
      user: {
        tel: '',
        name: ''
      }
    }
  },
  onLoad(option) {
    this.type = option.type;
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>