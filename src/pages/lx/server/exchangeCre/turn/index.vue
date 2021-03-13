<template>
  <view class="container">
    <view class="center">
      <view class="turner">
        <input type="number" placeholder="转账人卡号" :value="turner.card" />
        <input type="number" placeholder="转账人姓名" :value="turner.name"/>
      </view>
      <view class="receive">
        <input type="number" placeholder="受赠人卡号" :value="receive.card"/>
        <input type="number" placeholder="受赠人姓名" :value="receive.name"/>
      </view>
      <view class="num">
        <input type="number" placeholder="请输入积分数" :value="turnNum"/>
      </view>
      <button class="submit">转增</button>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      turner: {},
      receive: {},
      turnNum: ''
    }
  }
}
</script>

<style lang="less">
  @import './index.less';
</style>