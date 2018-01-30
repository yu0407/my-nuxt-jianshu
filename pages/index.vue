<template>
  <div>
  		<my-header></my-header>
  		<div class="index  my_container">
  				<div class="row">
  						<div class="col-8 main">
  					
  									<!-- 轮播图 -->
  									<div v-swiper:mySwiper="swiperOption" class="banner">
										    <div class="swiper-wrapper">
										      <div class="swiper-slide" v-for="banner in banners"> 	
										        <img :src="banner">
										      </div>
										    </div>
										   	<div class="swiper-pagination"></div>
										   	<div class="swiper-button-prev swiper-button-white"></div>
										   	<div class="swiper-button-next swiper-button-white"></div>
									
										</div>
										<!-- 推荐专题 -->
										<div class="recommend-collection">
												<nuxt-link to='/collection/123'>
													<img src="../static/collection1.png" alt="" />
													<span>旅行·在路上</span>
												</nuxt-link>
												
												<nuxt-link to='/collection/123'>
													<img src="../static/collection1.png" alt="" />
													<span>故事</span>
												</nuxt-link>
												
												<nuxt-link to='/collection/123'>
													<img src="../static/collection1.png" alt="" />
													<span>人文社科</span>
												</nuxt-link>
												<nuxt-link to='/collection/123'>
													<img src="../static/collection1.png" alt="" />
													<span>人文社科</span>
												</nuxt-link>
												<nuxt-link to='/collection/123'>
													<img src="../static/collection1.png" alt="" />
													<span>人文社科</span>
												</nuxt-link>
												<nuxt-link to='/collection/123'>
													<img src="../static/collection1.png" alt="" />
													<span>人文社科</span>
												</nuxt-link>
												
												<nuxt-link to='/collection/123' class='more_hot_collection'>
														更多热门专题
														<i class="fa fa-angle-right"></i>
												</nuxt-link>
										</div>
										<div class="split_line"></div>
										
										<!-- 文章列表 -->
										<div id="list_container">
											<ul class="note_list">
												<li class="have_img">
														<nuxt-link to='/'>
															<img src="../static/pic.jpg"/>
														</nuxt-link>
														<div class="content">
															 <div class="author">
															 		<nuxt-link to='/' class="avatar" href="">
															 			<img src="../static/userPic1.jpg" />
															 		</nuxt-link>
															 		<div class="info">
																 		<nuxt-link to='/'>测试用户</nuxt-link>
																		<span class="time">8小时前</span>
															 		</div>
															 </div>
															 <nuxt-link class='title' to='/'>
															 	如何把书中的知识转化成能力？这是我见过的最好回答
															 </nuxt-link>
															 <p class="abstract">
																	      随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，
																	      比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
															 </p>
															 <div class="meta">
															 		<nuxt-link to='/' class='collection_tag'>
															 			短片小说
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class=" fa fa-eye"></i>
															 			579
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class="fa fa-comment"></i>
															 			200
															 		</nuxt-link>
															 		<span><i class="fa fa-heart"></i>546</span>
															 </div>
														</div>
												</li>
												<li>
														<div class="content">
															 <div class="author">
															 		<nuxt-link to='/' class="avatar" href="">
															 			<img src="../static/userPic1.jpg" />
															 		</nuxt-link>
															 		<div class="info">
																 		<nuxt-link to='/'>测试用户</nuxt-link>
																		<span class="time">8小时前</span>
															 		</div>
															 </div>
															 <nuxt-link class='title' to='/'>
															 	如何把书中的知识转化成能力？这是我见过的最好回答
															 </nuxt-link>
															 <p class="abstract">
																	      随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，
																	      比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
															 </p>
															 <div class="meta">
															 		<nuxt-link to='/' class='collection_tag'>
															 			短片小说
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class=" fa fa-eye"></i>
															 			579
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class="fa fa-comment"></i>
															 			200
															 		</nuxt-link>
															 		<span><i class="fa fa-heart"></i>546</span>
															 </div>
														</div>
												</li>
												<li>
														<div class="content">
															 <div class="author">
															 		<nuxt-link to='/' class="avatar" href="">
															 			<img src="../static/userPic1.jpg" />
															 		</nuxt-link>
															 		<div class="info">
																 		<nuxt-link to='/'>测试用户</nuxt-link>
																		<span class="time">8小时前</span>
															 		</div>
															 </div>
															 <nuxt-link class='title' to='/'>
															 	如何把书中的知识转化成能力？这是我见过的最好回答
															 </nuxt-link>
															 <p class="abstract">
																	      随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，
																	      比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
															 </p>
															 <div class="meta">
															 		<nuxt-link to='/' class='collection_tag'>
															 			短片小说
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class=" fa fa-eye"></i>
															 			579
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class="fa fa-comment"></i>
															 			200
															 		</nuxt-link>
															 		<span><i class="fa fa-heart"></i>546</span>
															 </div>
														</div>
												</li>
												<li class="have_img">
														<nuxt-link to='/'>
															<img src="../static/pic.jpg"/>
														</nuxt-link>
														<div class="content">
															 <div class="author">
															 		<nuxt-link to='/' class="avatar" href="">
															 			<img src="../static/userPic1.jpg" />
															 		</nuxt-link>
															 		<div class="info">
																 		<nuxt-link to='/'>测试用户</nuxt-link>
																		<span class="time">8小时前</span>
															 		</div>
															 </div>
															 <nuxt-link class='title' to='/'>
															 	如何把书中的知识转化成能力？这是我见过的最好回答
															 </nuxt-link>
															 <p class="abstract">
																	      随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，
																	      比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
															 </p>
															 <div class="meta">
															 		<nuxt-link to='/' class='collection_tag'>
															 			短片小说
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class=" fa fa-eye"></i>
															 			579
															 		</nuxt-link>
															 		<nuxt-link to='/' class='tag'>
															 			<i class="fa fa-comment"></i>
															 			200
															 		</nuxt-link>
															 		<span><i class="fa fa-heart"></i>546</span>
															 </div>
														</div>
												</li>
											</ul>
										</div>  
  									<!-- 阅读更多 -->
  									<nuxt-link to='/' class='load-more'>阅读更多</nuxt-link>
  						</div>
  		
  						<div class="col-4 aside">
  								<div class="board">
  									<nuxt-link to='/'>
  											<img src="../assets/img/board_1.png" alt="" />
  									</nuxt-link>
  									<nuxt-link to='/'>
  											<img src="../assets/img/board_2.png" alt="" />
  									</nuxt-link>
  									<nuxt-link to='/'>
  											<img src="../assets/img/board_3.png" alt="" />
  									</nuxt-link>
  									<nuxt-link to='/'>
  											<img src="../assets/img/board_4.png" alt="" />
  									</nuxt-link>
  									<nuxt-link to='/'>
  											<img src="../assets/img/board_5.png" alt="" />
  									</nuxt-link>
  								</div>
  							
  								<nuxt-link to='/download' class='download' @mouseover.native='showQrcode = true' @mouseleave.native='showQrcode = false'>
	  									<transition>
		  										<div class="showQrcode" v-show='showQrcode'>
		  											<img src="../static/download.png"/>
		  										</div>
	  									</transition>
	  									<img src="../static/download.png"/>
	  									<div class="title">
		  										<p>
			  										下载简书手机App
			  										<i class="fa fa-angle-right"></i>
		  										</p>
		  										<p>随时随地发现和创作内容</p>
	  									</div>
  								</nuxt-link>
									<div class="recommend-author">
  									<div class="title">
  											<span>推荐作者</span>
  											<a href="javascript:void(0)" class="page-change" @click='route'>
  												<i class="fa fa-refresh" ref='refresh'></i>
  												换一批
  											</a>
  									</div>
  									<ul class="list">
  										<li>
  											<nuxt-link to='/' class='avatar'>
  												<img src="../static/userPic1.jpg"/>
  											</nuxt-link>
  											<nuxt-link to='/' class='name'>占小狼</nuxt-link>
  											<nuxt-link class='follow' to='/'>关注 <i class="fa fa-plus"></i></nuxt-link>
  											<p>写了70.6k字 · 10.9k喜欢</p>
  										</li>
  										<li>
  											<nuxt-link to='/' class='avatar'>
  												<img src="../static/userPic1.jpg"/>
  											</nuxt-link>
  											<nuxt-link to='/' class='name'>占小狼</nuxt-link>
  											<nuxt-link class='follow' to='/'>关注 <i class="fa fa-plus"></i></nuxt-link>
  											<p>写了70.6k字 · 10.9k喜欢</p>
  										</li>
  										<li>
  											<nuxt-link to='/' class='avatar'>
  												<img src="../static/userPic1.jpg"/>
  											</nuxt-link>
  											<nuxt-link to='/' class='name'>占小狼</nuxt-link>
  											<nuxt-link class='follow' to='/'>关注 <i class="fa fa-plus"></i></nuxt-link>
  											<p>写了70.6k字 · 10.9k喜欢</p>
  										</li>
  									</ul>
  									<nuxt-link to='/' class='find-more'>
  											查看全部 <i class="fa fa-angle-right"></i>
  									</nuxt-link>
  								</div>
  						</div>
  				</div>
  		</div>
  		<footer class="my_container">
  			<div class="row">
  				<div class="col-8">
  						<ul class="footer_list">
  							<li>
  								<nuxt-link to='/'>小余制作</nuxt-link>
  							</li>
  							<em> · </em>
  							<li>
  								<nuxt-link to='/'>联系我吧</nuxt-link>
  							</li>
  							<em> · </em>
  							<li>
  								<nuxt-link to='/'>我在河南</nuxt-link>
  							</li>
  							<em> · </em>
  							<li>
  								<nuxt-link to='/'>河南洛阳</nuxt-link>
  							</li>
  							<em> · </em>
  							<li>
  								<nuxt-link to='/'>嘻嘻嘻嘻</nuxt-link>
  							</li>
  							<em> · </em>
  							<li>
  								<nuxt-link to='/'>个人制作</nuxt-link>
  							</li>
  							<em> · </em>
  							<li>
  								<nuxt-link to='/'>QQ：763560703</nuxt-link>
  							</li>
  						</ul>
  				</div>
  			</div>
  		</footer>
  
  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader'
export default {
  head () {
    return {
      title: '简书-创作你的创作',
    }
  },
  data (){
  	return {
  		banners: ['/index_banner_2.jpg','/index_banner_2.jpg',
  		'/index_banner_3.jpg','/index_banner_4.jpg',
  		'/index_banner_5.jpg','/index_banner_6.jpg'],
        swiperOption: {
        		autoplay:{
        			delay:3000,
        			stopOnLastSlide:false,
        			disableOnInteraction:false
        		},
         	 	pagination: {
           		 el: '.swiper-pagination',
          	},
          	navigation:{
          		nextEl:'.swiper-button-next',
          		prevEl:'.swiper-button-prev'
          	}
          // some swiper options...
        },
        deg:360,
        showQrcode:false
  	}
  },
	mounted:function(){
		this.mySwiper.slideTo(3,1000,false)
	},
	methods:{
		route:function(){
			this.deg = this.deg + 360
			this.$refs.refresh.style.transform = `rotate(${this.deg}deg)`
		},
		add:function(){
			console.log(111)
		}
	},
  components:{
  	MyHeader,
  }
}
</script>

