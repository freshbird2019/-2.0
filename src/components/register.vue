<template>
<div id="register">
  <el-form :model="ruleForm" status-icon :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
    <p v-show="showTishi" align="center">{{tishi}}</p>
    <el-form-item label="用户名" :rules="[
      { required: true, message: '请输入用户名', trigger: 'blur' }]">
    <el-input v-model="ruleForm.username"></el-input>
  </el-form-item>

  <el-form-item label="密码" prop="pass" :rules="[
      { required: true, message: '请输入密码', trigger: 'blur' }]">
    <el-input type="password" v-model="ruleForm.pwd" autocomplete="off"></el-input>
  </el-form-item>
  <el-form-item label="确认密码" prop="checkPass">
    <el-input type="password" v-model="ruleForm.checkPass" autocomplete="off"></el-input>
  </el-form-item>
    <el-form-item label="电话" prop="phone" :rules="[
      { required: true, message: '请输入用户名', trigger: 'blur' }]">
      <el-input v-model.number="ruleForm.phone"></el-input>
    </el-form-item>
    <el-form-item
      prop="email"
      label="邮箱"
      :rules="[
      { required: true, message: '请输入邮箱地址', trigger: 'blur' },
      { type: 'email', message: '请输入正确的邮箱地址', trigger: ['blur', 'change'] }
    ]"
    >
      <el-input v-model="ruleForm.email"></el-input>
    </el-form-item>
  <el-form-item label="年龄" prop="age">
    <el-input v-model.number="ruleForm.age"></el-input>
  </el-form-item>
    <el-form-item label="性别" prop="sex">
      <el-input v-model.number="ruleForm.sex"></el-input>
    </el-form-item>
    <el-form-item label="住址" prop="address">
      <el-input v-model.number="ruleForm.address"></el-input>
    </el-form-item>
    <el-form-item label="所在医院" prop="hos">
      <el-input v-model.number="ruleForm.hospital"></el-input>
    </el-form-item>
  <el-form-item>
    <el-button type="primary" @click="Register(ruleForm)">提交</el-button>
    <el-button @click="resetForm(ruleForm)">重置</el-button>
  </el-form-item>
</el-form>
</div>
</template>
 
<script src="./js/register.js">

 
</script>
 
<style scoped src="./CSS/register.css">
 
</style>
