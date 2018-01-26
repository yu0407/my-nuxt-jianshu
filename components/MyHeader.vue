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
					<nuxt-link to='/signUp' class="btn sign-up">注册</nuxt-link>
					<nuxt-link to='/signIn' class="btn sign-in">登录</nuxt-link>
					<!-- 如果用户登录了 显示用户头像 -->
					<div style="display: none;" class="nav-user" @mouseover='userShow=true' @mouseleave="userShow = false">
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
					
					<div class="my_container">
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
							<li class="notify"  @mouseover='msgShow=true' @mouseleave="msgShow = false">
								<nuxt-link to='/'>
									<i class="fa fa-bell"></i>
									<span>消息</span>
								</nuxt-link>
								<div class="nav-drop-menu" v-show='msgShow'>
									<ul>
										<li>
											<nuxt-link to='/'>
												<i class="fa fa-comment-o"></i>
												<span>评论</span>
											</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>
												<i class="fa fa-envelope-o"></i>
												<span>简信</span>
											</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>
												<i class="fa fa-upload"></i>
												<span>投稿请求</span>
											</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>
												<i class="fa fa-heart-o"></i>
												<span>喜欢和赞</span>
											</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>
												<i class="fa fa-user-plus"></i>
												<span>关注</span>
											</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>
												<i class="fa fa-ellipsis-h"></i>
												<span>其他请求</span>
											</nuxt-link>
										</li>
									</ul>
								</div>
								
							</li>
							<!-- 头部导航搜索框 -->
							<li class="search search_wrap_active">
								<form method="post">
									<transition>
										<input type="text" placeholder="搜索" @focus='searchShow = true' @blur='searchShow = false' />
									</transition>
									<nuxt-link to='/' :class=" searchShow == true ? 'search_btn search_btn_active' : 'search_btn' ">
										<i class="fa fa-search"></i>
									</nuxt-link>
								</form>
								<div class="search_history" v-show='searchShow'>
									<p><span>热门搜索</span> <nuxt-link to='/'><i class="fa fa-refresh"></i>换一批</nuxt-link> </p>
									<ul>
										<li>
											<nuxt-link to='/'>PPT</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>旅行青蛙</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>旅行青蛙</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>旅行青蛙</nuxt-link>
										</li>
										<li>
											<nuxt-link to='/'>旅行青蛙</nuxt-link>
										</li>
									</ul>
								</div>
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
				searchShow:false,
				msgShow:false
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
	nav a.sign-in{
		float: right;
		width: 80px;
		height: 40px;
		margin:  11px 6px 0 10px;
		line-height: 24px;
		font-size: 15px;
		line-height: 24px;
		color: #969696 !important;
		box-shadow: none !important; 
	}
	nav a.sign-up{
		float: right;
		width: 80px;
		height: 40px;
		margin:  11px 6px 0 10px;
		line-height: 24px;
		font-size: 15px;
		border: solid 1px #EA6F5A;
		border-radius: 20px;
		padding: 6px;
		color: #EA6F5A !important; 
		line-height: 24px;
	}
	nav a.sign-up:hover{
		background: rgb(254,247,246);
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
		height: 100%;
		border-radius: 50%;
		border: solid 1px #ccc;
	}
	nav .nav-user .nav-drop-menu{
		left: 0;
		position: absolute;
		min-width: 160px;
		font-size: 15px;
		box-shadow: 0 0 8px rgba(0,0,0,.1);
	}
	nav .nav-user .nav-drop-menu ul{
		padding: 10px 0;
		margin: 0;
	}
	nav .nav-user .nav-drop-menu ul li a{
		display: block;
		padding:10px 15px;
	}
	nav .nav-user .nav-drop-menu ul li a:hover{
		background: #f5f5f5;
	}
	nav .nav-user .nav-drop-menu ul li i{
		margin-right: 15px;
		color: #EA6F5A;
		font-size: 18px;
	}
	
	nav .nav-list{
		padding: 0 !important;
		margin: 0 !important;
		zoom: 1;
		/*display: none;*/
	}
	nav .nav-list:after{
		content:'';
		height: 0;
		display: block;
		visibility: hidden;
		clear: both;
	}
	nav .nav-list > li{
		float: left;
		text-align: left;
		margin-right: 5px;
	}
	nav .nav-list > li:hover{
		background: #f5f5f5;
	}
	nav .nav-list > li.active > a{
		display: block;
		height: 55px;
		padding: 15px;
		font-size: 17px;
		color: #EA6F5A !important;
		
	}
	nav .nav-list > li.active{
		background: white;
	}
	nav .nav-list > li > a{
		height: 56px;
		padding:15px;
		margin-right: 15px;
		font-size: 18px;
		display: block;
	}
	nav .nav-list > li > a > i{
		margin-right: 7px;
		font-size: 20px;
		margin-top: 5px;
	}
	@media (max-width:1440px) {
        nav .nav-list>li>a i {
            display:none;
        }
    }
    @media (max-width:1080px) {
        nav .nav-list>li>a i {
            display:block;
        }
        nav .nav-list>li>a span {
            display:none;
        }
    }
	
	nav .nav-list .notify{
		position: relative;
	}
	nav .nav-list .notify .nav-drop-menu{
		position: absolute;
		top: 56px;
		left: 0;
		min-width: 160px;
		font-size: 15px;
		box-shadow: 0 0 8px rgba(0,0,0,.1);
		z-index: 9999;
	}
	nav .nav-list .notify .nav-drop-menu ul{
		padding: 10px 0;
		margin: 0;
	}
	nav .nav-list .notify .nav-drop-menu ul li a{
		display: block;
		padding:10px;
	}
	nav .nav-list .notify .nav-drop-menu ul li a:hover{
		background: #f5f5f5;
	}
	nav .nav-list .notify .nav-drop-menu ul li i{
		margin-right: 15px;
		color: #EA6F5A;
		font-size: 18px;
		margin-left: 10px;
	}


	
	nav .nav-list .search{
		padding-left: 15px;
		background: white !important;
		position: relative;
	}
	nav .nav-list .search form{
		margin-top: 9px;
		position: relative;
	}
	nav .nav-list .search form input{
		width: 240px;
		height: 38px;
		outline: none;
		border: none;
		background: rgb(238,238,238);
		border-radius: 40px;
		padding: 0 40px 0 20px;
		font-size: 14px;
		transition:width linear .35s;
	}
	nav .nav-list .search form input:focus{
		width: 320px;
	}
	nav .nav-list .search form .search_btn{
		position: absolute;
		right: 10px;
		top: 4px;
		width: 30px;
		height: 30px;
		text-align: center;
		border-radius: 50%;
		
	}
	nav .nav-list .search .search_btn i{
		line-height: 30px;
	}
	nav .nav-list .search form .search_btn_active{
		background: #969696;
		color: white !important;
	}
	
	
	

	nav .nav-list .search_history:before{
		content: '';
		top: -5px;
		left: 27px;
		width: 10px;
		height: 10px;
		z-index: 1;
		position: absolute;
		background: white;
		transform: rotate(45deg);
		
	}
	nav .nav-list .search_history{
		left: 0;
		top: 100%;
		width: 250px;
		margin-top:9px;
		position: absolute;
		background: white;
		border-radius: 4px;
		padding: 20px 20px 10px;
		box-shadow: 0 0 8px rgba(0,0,0,.2);
	}
	nav .nav-list  .search_history p{
		font-size: 14px;
		color: #969696;
	}
	nav .nav-list  .search_history p a{
		float: right;
	}
	nav .nav-list  .search_history p a i{
		margin-right:2px;
	}
	nav .nav-list  .search_history ul{
		overflow: hidden;
	}
	nav .nav-list  .search_history ul li{
		float: left;
		margin-right: 10px;
		line-height: 28px;
	}
	nav .nav-list  .search_history ul li a{
		border: solid 1px rgb(221,221,221);
		border-radius: 3px;
		color: rgb(120,120,120)!important;
		font-size: 12px;
		padding:2px 6px;
		
	}
	
	@media (max-width:1440px ) {
		nav .nav-list > li > a > i{
			display: none;
		}
		nav .nav-list .search form input{
			width: 160px;
		}
		nav .nav-list .search form input:focus{
			width: 240px;
		}
	}
	
	@media (max-width:1080px ) {
		nav .nav-list li a span{
			display: none;
		}
		nav .nav-list li a i{
			display: block;
		}
		nav .nav-list .search form input{
			width: 150px;
		}
		nav .nav-list .search form input:focus{
			width: 150px;
		}
	}
	@media (max-width:820px ) {
		nav .nav-list li{
			display: none;
		}
	}
	
</style>