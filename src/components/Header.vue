<template>
  <div >
    <div class="line"></div>
    <el-menu
      :default-active="activeIndex2"
      class="el-menu-demo"
      mode="horizontal"
      @select="handleSelect"
      background-color="#1B9CFC"
      text-color="#fff"
      active-text-color="#182C61">
      <el-menu-item index="1" @click="clickRouter(2)" v-bind:class="{ bind_underline:where===2 }" style="margin:0px 10px 0px 10px;font-size: 20px">首页</el-menu-item>
      <el-menu-item index="1" v-bind:class="{bind_underline:where===3}"  @click="clickRouter(3)" style="margin:0px 10px 0px 10px;font-size: 20px">肿块识别训练</el-menu-item>
      <el-menu-item index="1" v-bind:class="{ bind_underline:where===4 }"  @click="clickRouter(4)" style="margin:0px 10px 0px 10px;font-size: 20px">辅助诊疗</el-menu-item>

      <el-menu-item index="1" @click="clickRouter(0)"  @mouseover="changeMaska(true)" @mouseout="changeMaska(false)" style="margin:0px 10px 0px 10px;font-size: 20px">登陆</el-menu-item>
      <el-menu-item index="1" @click="clickRouter(1)"  @mouseover="changeMaskb(true)" @mouseout="changeMaskb(false)" style="margin:0px 10px 0px 10px;font-size: 20px">注册</el-menu-item>

      <el-submenu index="2" style="margin:0px 10px 0px 10px;font-size: 20px">
        <template slot="title" >乳腺癌防治</template>
        <el-menu-item index="2-1">最新信息</el-menu-item>
        <el-menu-item index="2-2">论坛</el-menu-item>
        <el-menu-item index="2-3">求助</el-menu-item>
      </el-submenu>
    </el-menu>

  </div>
</template>

<script src="./js/Header.js">
  export default {
    data() {
      return {
        activeIndex: '1',
        activeIndex2: '1'
      };
    },
    methods: {
      handleSelect(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }

</script>

<style scoped src="./CSS/Header.css">


</style>


