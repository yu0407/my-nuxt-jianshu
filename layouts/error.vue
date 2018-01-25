<template>
  <div class="error">
  	<div class="error-logo">
  		<nuxt-link to='/'><img src="../assets/img/errorLogo.png"/></nuxt-link>
  	</div>
  	<div class="error-wrap">
  			<div class="error-content">
  				<img src="../assets/img/error.png"/>
  				<h3>您要找的页面不存在</h3>
  				<p>可能是因为您的链接地址有误、该文章已经被作者删除或转为私密状态。</p>
  				<nuxt-link to='/'> 返回「简书」首页 </nuxt-link>
  			</div>
  			<div class="error-footer">
  				
  			</div>
  			<!--<h1>4</h1>
  			<h2>0</h2>
  			<h3>4</h3>-->
  	</div>
  </div>
</template>
<script>
	import '@/assets/css/error.css'
export default {
  props: ['error'],
  head() {
  	return{
  		title:'您要找的页面不存在-简书'
  	}
  }
}
</script>

<style scoped>
.title
{
  margin-top: 15px;
  font-size: 5em;
}
.info
{
  font-weight: 300;
  color: #9aabb1;
  margin: 0;
}
.button
{
  margin-top: 50px;
}
</style>
