<template>
  <div id="test">
  <el-container>
    <el-steps :space="200" :active="active" simple finish-status="success">
      <el-step title="声明" icon="el-icon-edit"></el-step>
      <el-step title="上传图片" icon="el-icon-upload"></el-step>
      <el-step title="预览图片" icon="el-icon-picture"></el-step>
    </el-steps>

    <el-main style="height:525px;">
    <router-view></router-view>
    </el-main>
    <el-footer  style="padding:0;border:0;height:35px;">
        <div id="buttons">

            <el-button-group>
            <el-button type="primary" icon="el-icon-arrow-left" v-if="active>0" @click="front()">上一页</el-button>
            <el-button type="primary" @click="next()" v-if="active<2">下一页<i class="el-icon-arrow-right el-icon--right"></i></el-button>
            </el-button-group>
            <el-button class="submit" type="primary" @click="open" v-if="active==2">提交</el-button>

            </div>
    </el-footer>

    </el-container>
  </div>
</template>

<script>
export default{
    data(){
        return{
            router_dre:['/test/','/test/step2','/test/step3'],
            active:0,

        };
    },
    methods:{
        next() {
        this.active++;
        //alert(this.router_dre[this.active]);
        this.$router.push({path:this.router_dre[this.active]});
        },
        front(){
        if (this.active-- < 0) this.active = 0;
        this.$router.push({path:this.router_dre[this.active]});
        },
        //上传到后台的图片-------
        /*将"imgs"上传 */
        submits(){
            this.$router.push({path:'/step4'});
        },
        //---------------------
        upLoad(){
            this.submits();
            //alert("成功");
        },
         open() {
        this.$confirm('是否上传图片?', '提示', {
          confirmButtonText: '确定',
          cancelButtonText: '取消',
          type: 'warning'
        }).then(() => {
          this.$message({
            type: 'success',
            message: '上传成功!'
          });
          this.upLoad();
        }).catch(() => {
          this.$message({
            type: 'info',
            message: '已取消上传'
          });
        });
      }
    }

}
</script>

<style  scoped >
#test{
    //background-color:red;
    //height: 1000px;
    width: -webkit-fill-available;
}
.el-main{
    width: -webkit-fill-available;
}
.el-header{
    //background-color:red;
}
#buttons{
    //background-color:red;
    float:right;
}
.el-main{
    //background-color:red;
}
</style>
