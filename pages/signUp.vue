<template>
  <div class="sign"> 
    <!--logo-->
    <div class="logo">
     <!--代替a链接-->
     <nuxt-link to="/">
      <img src="../assets/img/logo.png" alt="">
     </nuxt-link>
    </div>

    <!--注册表单-->
  	<div class="main">
	  	<div class="title">
	        <h4>
                <nuxt-link to="/signIn" > 登录 </nuxt-link>
                 <b>·</b>
                <nuxt-link to="/signUp" class="active"> 注册 </nuxt-link>
	        </h4>
	    </div>
  		<div class="js-sign-up">
  			<form method="post">
  				<div class="input-prepend">
  					<input type="text" name="" id="" value=""placeholder="你的昵称" class="top-radius" />
  					<i class="fa fa-user"></i>
  				</div>
  				<div class="input-prepend">
  					<input type="text" name="" id="" value="" placeholder="手机号" />
  					<i class="fa fa-phone"></i>
  				</div>
  				<div class="input-prepend ssm">
  					<input type="" name="" id="" value="" placeholder="请输入验证码" />
  					<i class="fa fa-shield"></i>
  					<a class="send-ssm btn btn-success" href="#">发送验证码</a>
  				</div>
  				<div class="input-prepend">
  					<input type="password" name="" id="" value=""  class="bottom-radius" placeholder="设置密码"/>
  					<i class="fa fa-lock"></i>
  				</div>
  				<input type="submit" value="注册" class="btn btn-success sign-up-btn"/>
  				<p class="sign-up-msg">
  					点击 “注册” 即表示您同意并愿意遵守简书<br>
  					<a href="#">用户协议</a>
  					和
  					<a href="#">隐私政策</a>
  				</p>
  			</form>
  		</div>
  		 <div class="more-sign">
         		<p>社交账号注册</p>
         		<ul>
         			<li class="weixin">
         				<a href="#">
         					<i class="fa fa-weixin"></i>
         				</a>
         			</li>
         			<li class="qq">
         				<a href="#">
         					<i class="fa fa-qq"></i>
         				</a>
         			</li>
         			
         		</ul>
         </div>
       </div>
  		
  	</div>

   </div>
</template>
<script>
import '@/assets/css/sign.css'
import '@/assets/css/font-awesome.min.css'
export default {
   layout:'sign',//指明当前页面使用的模板是sign
 head(){
     return{
         title:'登录 - 简书',
         meta:[
             {hid:'description',name:'description',content:'登录页面'}
         ]
     }
 },
}
</script>
<style scoped>
.sign{
    /* 先写盒子模型 然后文本 定位放上面 */
    height: 100%;
    font-size: 14px;
    text-align: center;
    background: #f1f1f1;
}
/* logo */
.logo{
    position: absolute;
    top: 55px;
    left: 50px;
}
.logo img{
    width: 100px;
}
/* 登录盒子 */
.main{
    width: 400px;
    /*height: 500px;*/
    margin: 60px auto 0;
    background-color: white;
    border-radius: 4px;
    box-shadow: 0 0 8px rgba(0, 0, 0, .1) ;
    padding: 50px 50px 30px;
    display: inline-block;
}

.main .title{
    margin: 0 auto 50px;
    padding: 10px;
    color: #939393;
   
}
.main .title h4{
    margin:0;
    font-size: 18px;
}
.main .title h4 a,
.main .title h4 b{
    padding: 10px;
}
.main .title h4 a.active{
    font-weight: 700;
    color: #ea6f5a !important;
    border-bottom:2px solid #ea6f5a;
}
.main  .title h4 a:hover{
    border-bottom:2px solid #ea6f5a;
}

/* form */
.main form{
    margin: 0 0 30px;
    color: rgb(120,120,120);
}
.main form .input-prepend{
    position: relative;
    width: 100%;
}
.main form .input-prepend input{
    width: 100%;
    height: 50px;
    padding: 4px 12px 4px 35px;
    border: 1px solid #c8c8c8;
    border-bottom: none;
    background-color: rgb(248,248,248);
}
.main .top-radius{
	border-radius: 4px 4px 0 0;
}
.main form input.bottom-radius{
	border-bottom: solid 1px #C8C8C8;
	border-radius: 0 0 4px 4px ;
}
.main form .input-prepend i{
    position: absolute;
    color:#969696;
    top:16px;
    left:15px;
    font-size:20px;
}

.main form .remember{
	float: left;
	margin: 25px 0;
}

.main form .help{
	float: right;
	margin: 25px 0;
}
.main form > input{
	width: 100%;
	display: block;
	border-radius: 5px;
}
.main .more-sign p{
	position: relative;
	font-size: 14px;
	color: #b8b8b8;
	margin-bottom: 20px;
}
.main .more-sign p:before,.main .more-sign p:after{
	content: '';
	width: 60px;
	border-bottom: solid 1px #B8B8B8;
	position: absolute;
	top: 10px;
}
.main .more-sign p:after{
	right: 30px;
}
.main .more-sign p:before{
	left: 30px;
}

.main .more-sign ul{
	margin-bottom: 20px;
}
.main .more-sign ul li{
	display: inline-block;
	margin: 0 3px;
}
.main .more-sign ul li.weibo a{
	background: rgb(224,82,68);
}
.main .more-sign ul li.weixin a{
	background: rgb(0,187,41);
}
.main .more-sign ul li.qq a{
	background:rgb(73,138,213);
}
.main .more-sign ul li.another a{
	background: rgb(240,240,240);
	color: rgb(120,120,120) !important;
}
.main .more-sign ul li a{
	width: 50px;
	height: 50px;
	display: block;
	border-radius: 50%;
	line-height: 50px;
	/*background: gray;*/
}
.main .more-sign ul li a i{
	color: white;
	font-size: 20px;
}

@media (max-width:768px){
	.logo{
		display: none;
	}
	.sign{
		background: #FFFFFF;
	}
	html,body{
		background: #FFFFFF !important;
	}
	.main{
		box-shadow: none;
		margin: 0 auto;
	}
}
.sign-up-btn{
	margin-top: 20px;
}
.sign-up-msg{
	margin: 10px 0;
	text-align: center;
	font-size: 12px;
	color: #969696;
	line-height: 20px;
}
.sign-up-msg a{
	color: #3388ff !important;
}
.main form .ssm{
	position: relative;
	display: none;
}
.main form .input-prepend a.send-ssm{
	position: absolute;
	width: 100px;
	height: 36px;
	right: 7px;
	top: 7px;
	color: white !important;
	background: rgba(157,220,147);
	border: solid 1px lightgray;
	font-size: 13px;
	border-radius: 20px;
}











	
</style>