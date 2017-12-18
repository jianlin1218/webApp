<template>
    <div name="right">
      <tab v-model="index">
        <tab-item class="vux-center" :selected="curTab === item" v-for="(item, index) in tabList" @click="curTab = item" :key="index">{{item}}</tab-item>
      </tab>
      <swiper v-model="index" height="100px" :show-dots="false">
        <swiper-item v-for="(item, index) in tabList" :key="index">
          <div class="tab-swiper vux-center">{{item}} Container</div>
        </swiper-item>
      </swiper>
    </div>
</template>

<script>
  import {Group, Tab, TabItem, Swiper, SwiperItem} from 'vux'
  const list = () => ['精选', '美食', '电影', '酒店', '外卖']

  export default {
    components: {
      Group,
      Tab,
      TabItem,
      Swiper,
      SwiperItem
    },
    data () {
      return {
        msg: 'Hello World!',
        tabList: list(),
        index: 1,
        curTab: '美食'
      }
    },
    methods: {
      onItemClick (index) {
        console.log('on item click:', index)
      }
    }
  }
</script>

<style>
  div {

  }
</style>
