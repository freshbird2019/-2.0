<template>
  <div id="app">
    <!-- 其他页 -->
    <el-container>
      <el-header style="padding:0px;margin-bottom:0px;">
        <!-- 导航栏 -->
          <header-nav ></header-nav>
      </el-header>

      <el-main >
        <!-- Body -->
         <router-view></router-view>
      </el-main>
    </el-container>

    <el-footer>
      <Footer style="height: 50px"></Footer>
    </el-footer>
   </div>
</template>

<script>
import header from './components/Header.vue';
import Footer from './components/Footer.vue';
export default{
    data(){
        return{

        };
    },
    components: {
        headerNav: header,
        Footer:Footer,
    }
}

</script>

<style scoped>
 #app{
  width:100%;
  height: -webkit-fill-available;
 }
 .el-container{
  //background-color: red;
 }
 .el-container>.el-container{

 }
 .el-main{
  margin: 5px;
 }
 .el-footer{
  //background-color: blue;
 }
 .Footer{
 }

</style>
