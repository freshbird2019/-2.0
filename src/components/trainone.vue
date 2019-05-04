<template>
  <el-main style="padding:0;border:0;">
    <div id="img_name">
      <ul>
        <li><div><img :src="avatar" class=""></div></li>
      </ul>
    </div>
  </el-main>
</template>

<script>
    export default {
        name: "trainone",
      data(){
          return{
            avatar:'',
            piclocal:''
          }
      },
      mounted() {
        this.piclocal = this.$route.query.piclocal;
        console.log(this.piclocal);
        this.avatar = require("../../static/trainPic/" + this.piclocal + ".jpg")
      }
    }
</script>

<style scoped src="./CSS/step2.css">

</style>
