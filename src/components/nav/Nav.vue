<template>
  <el-menu
      router
      mode="horizontal"
      background-color="#7F95D1"
      text-color="#fff"
      active-text-color="#d7dcef"
      :default-actie="$route.path">
    <el-menu-item v-for="item in menuData" :key="item.name" :index="item.routerPath">
      <template slot="title">
        <i :class=item.icon style="color: #d7dcef" ></i>
        {{ item.name }}
      </template>
    </el-menu-item>
  </el-menu>

</template>

<script>

export default {
  name: "Nav",
  data() {
    return {
      menuData: [
        {
          name: "首页", icon: "el-icon-s-data", routerPath: "/data"
        },
        {
          name: "捐赠动态", icon: "el-icon-s-promotion", routerPath: "/donation"
        },
        {
          name: "需求动态", icon: "el-icon-s-flag", routerPath: "/demand"
        },
        {
          name: "投票表决", icon: "el-icon-s-claim", routerPath: "/vote"
        },
        // {
        //   name: "NFT", icon: "el-icon-present", routerPath: "/about"
        // },
      ]
    }
  },
}
</script>

<style scoped>

</style>