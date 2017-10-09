<style lang="scss" scoped>
.g-content {
  padding-top: 40px;
  &.up{
    padding-bottom: 50px; 
  }
}
</style>

<template>
  <div>
    <!-- 头部: Mint-Header 组件 -->
    <mt-header fixed :title="title"></mt-header>

    <!-- 内容容器 -->
    <div class="g-content up">
      <!-- <customer-list></customer-list> -->
      <index-tab></index-tab>
    </div>
    <!-- /内容容器 -->

    <!-- 列表 -->

    <!-- 底部 Tab: Mint-Tabbar 组件 v-model="selected"-->
    <mt-tabbar> 
      <mt-tab-item id="首页">
        <img slot="icon" src="../assets/tab-icons/tab-home.png"> 首页
      </mt-tab-item>
      <mt-tab-item id="业务">
        <img slot="icon" src="../assets/tab-icons/tab-work.png"> 业务
      </mt-tab-item>
      <mt-tab-item id="客户">
        <img slot="icon" src="../assets/tab-icons/tab-client.png"> 客户
      </mt-tab-item>
      <mt-tab-item id="对话">
        <img slot="icon" src="../assets/tab-icons/tab-message-active.png"> 对话
      </mt-tab-item>
      <mt-tab-item id="我">
        <img slot="icon" src="../assets/tab-icons/tab-me.png"> 我
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>

<script>
import Vue from 'vue'
import { Header, Tabbar, TabItem, Search } from 'mint-ui'
import IndexTab from '@/pages/IndexTab'
Vue.component(Header.name, Header)
Vue.component(Header.name, Search)
Vue.component(Tabbar.name, Tabbar)
Vue.component(TabItem.name, TabItem)

export default {
  name: 'ClientTab',
  components:{
    IndexTab
  },
  data() {
    return {
      title: '首页'
    }
  }
}
</script>