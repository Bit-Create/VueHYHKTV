<template>
  <div>
    <tab-bar>
      <tab-bar-item link="/home">
        <template v-slot:item-text>
          <div>首页</div>
        </template>
      </tab-bar-item>
      <tab-bar-item link="/room">
        <template v-slot:item-text>
          <div>房间管理</div>
        </template>
      </tab-bar-item>
      <tab-bar-item link="/member">
        <template v-slot:item-text>
          <div>会员信息</div>
        </template>
      </tab-bar-item>
      <tab-bar-item link="/record">
        <template v-slot:item-text>
          <div>记录查询</div>
        </template>
      </tab-bar-item>
      <tab-bar-item  link="/about">
        <template v-slot:item-text>
          <div>关于</div>
        </template>
      </tab-bar-item>
    </tab-bar>
    <router-view></router-view>
  </div>
</template>

<script>
import TabBar from "@/components/tabbar/TabBar";
import TabBarItem from "@/components/tabbar/TabBarItem";
export default {
name: "MainBar",
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style scoped>

</style>