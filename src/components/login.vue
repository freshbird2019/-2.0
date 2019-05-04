
<template xmlns="http://www.w3.org/1999/html">
  <div>
    <div class="limiter">
      <div class="container-login100" >
        <div class="wrap-login100 p-l-110 p-r-110 p-t-62 p-b-33">
          <form class="login100-form validate-form flex-sb flex-w">

            <div style="width:100%;">

              <a href="#" class="btn-face m-b-20" style="margin: 0 50px 0 0">
                <img style="width: 50px; margin: 0 20px 0 0" src="./login/images/icons/wechat.png" alt="GOOGLE" >
                微信
              </a>

              <a href="#" class="btn-google m-b-20">
                <img style="width: 50px; margin: 0 20px 0 0" class="resize" src="./login/images/icons/QQ.png" alt="GOOGLE" >
                QQ
              </a>
            </div>


            <div class="p-t-31 p-b-9">
						<span class="txt1">
							用户名
						</span>
            </div>
            <div class="wrap-input100 validate-input" data-validate = "Username is required">
              <input class="input100" type="text" name="username" >
              <span class="focus-input100"></span>
            </div>

            <div class="p-t-13 p-b-9">
						<span class="txt1">
							密码
						</span>

              <a href="#" class="txt2 bo1 m-l-5">
                忘记密码?
              </a>
            </div>
            <div class="wrap-input100 validate-input" data-validate = "Password is required">
              <input class="input100" type="password" name="pass" >
              <span class="focus-input100"></span>
            </div>

            <div class="container-login100-form-btn m-t-17">
              <button class="login100-form-btn">
                登陆
              </button>
            </div>

            <div class="w-full text-center p-t-55">

              <a href="#" class="txt2 bo1">
                还没有注册？
              </a>
            </div>
          </form>
        </div>
      </div>
    </div>

  </div>
</template>

<!--===============================================================================================-->
<script src="src/components/login/vendor/jquery/jquery-3.2.1.min.js"></script>
<!--===============================================================================================-->
<script src="src/components/login/vendor/animsition/js/animsition.min.js"></script>

<!--===============================================================================================-->
<script src="src/components/login/vendor/bootstrap/js/popper.js"></script>
<script src="src/components/login/vendor/bootstrap/js/bootstrap.min.js"></script>
<!--===============================================================================================-->
<script src="src/components/login/vendor/select2/select2.min.js"></script>
<!--===============================================================================================-->
<script src="src/components/login/vendor/daterangepicker/moment.min.js"></script>
<script src="src/components/login/vendor/daterangepicker/daterangepicker.js"></script>
<!--===============================================================================================-->
<script src="src/components/login/vendor/countdowntime/countdowntime.js"></script>
<!--===============================================================================================-->
<script src="src/components/login/js/main.js"></script>

<script type="javascript">

</script>
<!--<style scoped type="text/css" src="./login/images/icons/favicon.ico"></style>-->
<style src="./login/vendor/bootstrap/css/bootstrap.min.css"/>
<style src="./login/fonts/font-awesome-4.7.0/css/font-awesome.min.css"/>
<style src="./login/vendor/animate/animate.css"/>
<style src="./login/vendor/css-hamburgers/hamburgers.min.css"/>
<style src="./login/vendor/animsition/css/animsition.min.css"/>
<style src="./login/vendor/daterangepicker/daterangepicker.css"/>
<style src="./login/css/util.css"/>
<style src="./login/css/main.css"/>
<style scoped type="text/css" src="./login/vendor/select2/select2.min.css">
  img.resize {
    height:50px;
    width:auto;
  }
</style>
