<template>
  <div>
  		<my-header></my-header>
  		<div>
  			按时到敬爱回家圣诞节啊
  		</div>
  </div>
</template>

<script>
import MyHeader from '@/components/MyHeader'
export default {
  head () {
    return {
      title: '简书-创作你的创作'
    }
  },
  components:{
  	MyHeader
  }
}
</script>

<style scoped>
.title
{
  margin: 30px 0;
}
.users
{
  list-style: none;
  margin: 0;
  padding: 0;
}
.user
{
  margin: 10px 0;
}
</style>
