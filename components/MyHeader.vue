<template>
	<div>
		<nav class="navbar navbar-default nav-fixed-top">
			<div class="nav-width-limit">
					<nuxt-link to='/' class='nav-logo'>
						<img src="../assets/img/navLogo.png"/>
					</nuxt-link>
					<!-- 写文章 -->
					<nuxt-link to='/' class='btn nav-write-btn'>
						<i class="fa fa-pencil"></i>写文章
					</nuxt-link>
					<!-- 如果用户登录了 显示用户头像 -->
					<div class="nav-user" @mouseover='userShow=true' @mouseleave="userShow = false">
						<div class="nav-drop-down" >
							<nuxt-link class='nav-avatar' to='/users'  >
								<img src="../assets/img/default-avatar.jpg"/>
							</nuxt-link>
						</div>
						<div class="nav-drop-menu"  v-show='userShow'>
							<ul>
								<li>
									<nuxt-link to='/'>
										<i class="fa fa-home"></i>
										我的主页
									</nuxt-link>
								</li>
								<li>
									<nuxt-link to='/'>
										<i class="fa fa-bookmark"></i>
										收藏的文章
									</nuxt-link>
								</li>
								<li>
									<nuxt-link to='/'>
										<i class="fa fa-heart"></i>
										喜欢的文章
									</nuxt-link>
								</li>
								<li>
									<nuxt-link to='/'>
										<i class="fa fa-cog"></i>
										设置
									</nuxt-link>
								</li>
								<li>
									<nuxt-link to='/'>
										<i class="fa fa-sign-out"></i>
										退出
									</nuxt-link>
								</li>
							</ul>
						</div>
					</div>
					<div class="container">
						<ul class="nav-list">
							<li class='active'>
								<nuxt-link to='/' >
									<i class="fa fa-compass"></i>
									<span>发现</span>
								</nuxt-link>
							</li>
							<li>
								<nuxt-link to='/'>
									<i class="fa fa-book"></i>
									<span>关注</span>
								</nuxt-link>
							</li>
							<li>
								<nuxt-link to='/'>
									<i class="fa fa-bell"></i>
									<span>消息</span>
								</nuxt-link>
							</li>
						</ul>
					</div>
			</div>
			
		</nav>
	</div>
</template>

<script>
	export default{
		name:'MyHeader', //这个组件命名
		data () {
			return{
				userShow:false,
				
			}
		}
	}
</script>

<style scoped>
	nav{
		height: 56px;
		width: 100%;
		padding: 0 !important;
		border-bottom: solid 1px #f0f0f0;
	}
	nav .navbar{
		margin-bottom: 20px;
		background: #FFFFFF;
	}
	nav .nav-fixed-top{
		position: fixed;
		left: 0;
		top: 0;
		z-index: 9999;
	}
	nav .nav-width-limit{
		width: 1440px;
		min-width: 768px;
		margin: auto;	
	}
	nav .nav-logo{
		width: 100px;
		float: left;
		height: 56px;
	}
	nav .nav-write-btn{
		float: right;
		width: 100px;
		height: 40px;
		font-size: 16px;
		color: white !important;
		border-radius: 20px;
		line-height: 24px;
		background: #ea6f5a;
		opacity: .9;
		margin: 8px 15px 0;
	}
	nav .nav-write-btn:hover{
		background: #ec6149;
	}
	nav .nav-user{
		float: right;
		position: relative;
	}
	nav .nav-user:hover{
		background: #f5f5f5;
	}
	nav .nav-user .nav-avatar{
		width: 40px;
		height: 40px;
		display: block;
		margin: 8px 28px 8px 20px;
		position: relative;
	}
	nav .nav-user .nav-avatar:before{
		content: "";
        position: absolute;
        top: 18px;
        right: -14px;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-top: 6px solid #999;
	}
	nav .nav-user .nav-avatar img{
		width: 100%;
		border-radius: 50%;
		border: solid 1px #ccc;
	}
	nav .nav-user .nav-drop-menu{
		position: absolute;
		left: 0;
		min-width: 160px;
		font-size: 14px;
		border: solid 1px lightgray;
		
	}
	nav .nav-user .nav-drop-menu ul{
		padding: 10px 0;
		margin: 0;
	}
	nav .nav-user .nav-drop-menu ul li a{
		display: block;
		padding:10px;
	}
	nav .nav-user .nav-drop-menu ul li a:hover{
		background: #f5f5f5;
	}
	nav .nav-user .nav-drop-menu ul li i{
		margin-right: 15px;
		color: #EA6F5A;
		font-size: 18px;
		margin-left: 10px;
	}
	nav .container{
		padding-left:15px;
		padding-right: 15px;
	}
	nav .nav-list{
		overflow: hidden;
		zoom: 1;
	}
	nav .nav-list li{
		float: left;
		text-align: left;
	}
	nav .nav-list li.active a{
		color: #EA6F5A !important;
	}
	nav .nav-list li a{
		height: 56px;
		padding:15px;
		margin-right: 15px;
		font-size: 18px;
		display: block;
	}
	
	nav .nav-list li a i{
		margin-right: 7px;
		font-size: 20px;
	}
	
	@media (max-width:1440px ) {
		nav .nav-list li a i{
			display: none;
		}
	}
	@media (max-width:1080px ) {
		nav .nav-list li a span{
			display: none;
		}
		nav .nav-list li a i{
			display: block;
		}
	}
</style>