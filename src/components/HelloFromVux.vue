<template>
  <div name="myapp" style="height:100%;">
    <div class="vux-demo">
      <img class="logo" src="../assets/vux_logo.png">
      <h1>web小程序</h1>
    </div>
    <group title="cell demo">
      <cell title="VUX" value="cool" is-link ></cell>
      <cell inline-desc="menerqiongse" link="http://www.baidu.com" title="anglar" value="aiyoweo" is-link ></cell>
    </group>
    <!--<x-header :right-options="{showMore: true}" @on-click-more="showMenus = true">with more menu</x-header>
    <div>
      <div style="height:44px;">
        <sticky scroll-box="vux_view_box_body" ref="sticky" :offset="46">
          <tab :line-width="1">
            <tab-item selected>正在正映</tab-item>
            <tab-item>即将上映</tab-item>
            <tab-item>已下线</tab-item>
          </tab>
        </sticky>
      </div>
      <div class="vux-demo">
        <img class="logo" src="../assets/vux_logo.png">
        <h1>web小程序</h1>
      </div>
      <group title="cell demo">
        <cell title="VUX" value="cool" is-link ></cell>
        <cell inline-desc="menerqiongse" link="http://www.baidu.com" title="anglar" value="aiyoweo" is-link ></cell>
      </group>
    </div>-->
  </div>
</template>

<script>
import { XHeader, Group, Cell, Tab, TabItem, Sticky, ViewBox } from 'vux'

export default {
  components: {
    XHeader,
    Group,
    Cell,
    Tab,
    TabItem,
    Sticky,
    ViewBox
  },
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 'Hello World!',
      menus: {
        menu1: 'Take Photo',
        menu2: 'Choose from photos'
      },
      showMenus: false
    }
  }
}
</script>

<style>
  html, body {
    height: 100%;
    width: 100%;
    overflow-x: hidden;
  }
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
</style>
