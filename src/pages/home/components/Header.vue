<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arror-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  overflow hidden
  line-height: $headerHeight;
  background: $bgColor;
  color: #ffffff;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      text-align: center;
      font-size: 0.4rem;
    }
  }

  .header-input {
    flex: 1;
    height: 0.64rem;
    line-height: 0.64rem;
    margin-top: 0.12rem;
    padding-left: 0.2rem;
    background: #fff;
    border-radius: 0.1rem;
    color: #cccccc;
  }

  .header-right {
    min-width: 1.04rem;
    padding: 0 .1rem
    float: right;
    text-align: center;
    color: #fff;

    .arror-icon {
      margin-left: 0.04rem;
      font-size: 0.24rem;
    }
  }
}
</style>
