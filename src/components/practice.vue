<template>
<div id="practice">
    <el-container>
        <el-header style="background-color:red;">
        </el-header>

        <el-main style="height:525px;background-color:green;">
          <!-- 未训练图片汇总 -->
          <el-table
            :data="tableData"
            style="width: 100%">
            <el-table-column
              label="序号"
              prop="trainpicid">
            </el-table-column>
            <el-table-column
              label="图片名称"
              prop="local">
            </el-table-column>
            <el-table-column
              label="图片大小"
              prop="size">
            </el-table-column>
            <el-table-column
              label="操作"
              prop="desc">
              <template slot-scope="scope">
                <el-button type="info"  size="mini" @click="Train(scope.row)"style="background:#C19892;border:none">训练</el-button>
              </template>
            </el-table-column>
          </el-table>


        </el-main>

        <el-footer  style="padding:0;border:0;height:35px;background-color:blue;">
        </el-footer>

    </el-container>
</div>
</template>
 
<script>
import {getCookie} from "./js/cookie";

export default{
  data() {
    return {
      userid:getCookie("userid"),
      tableData: [],
    }
  },
    methods:{
        Train(pic){
          let local=pic.local;
          this.$router.push({
            path: '/trainone',
            query: {
              piclocal:local
            }
          })
        }
    },
  mounted(){
    //加载训练图片信息
    console.log("loading data.");
    console.log(this.userid);
      let id=this.userid;
    if(id==="")id=1;
    this.$ajax.get( 'http://127.0.0.1:8088/project/notrainedpic/'+id
    ).then(response=>{
      console.log(response.data);
      for(let i= 0; i<response.data.length;i++) {
        this.tableData.push(response.data[i]);
      }
    });
  }

}
</script>
 
<style  scoped>
.el-main{
    width: -webkit-fill-available;
}
</style>
