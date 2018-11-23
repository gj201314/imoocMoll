<template>
  <div>
    <h3>这是商品列表页面</h3>
    {{$route.params}}
    <router-link to="/goods/title">显示商品标题</router-link>
    <router-link to="/goods/image">显示商品图片</router-link>
    <div>
      <router-view></router-view>
    </div> 
    <router-link to="/cart">router-link跳转到购物车页面</router-link>
    <button type="button" @click="tojump">button通过事件跳转到购物车页面</button>
  </div>
</template>
<script>
  export default {
    data(){
      return {
        msg:"Hello World"
      }
    },
    methods:{
      tojump(){
        //第一种 this.$router.push('/cart')
        //第二种 this.$router.push({'path':'/cart'});
        //第三种 this.$router.push({'path':'/cart?id=郭杰'});
        this.$router.push({'name':'Cart',params:{id:'傅永光'}});
      }
    }
  }
</script>
<style scoped>
  
</style>