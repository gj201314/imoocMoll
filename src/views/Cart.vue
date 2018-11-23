<template>
  <div>
    <h3>这里是购物车页面</h3>
    <p>query:{{$route.query}}</p>
    <p>params:{{$route.params}}</p>
  </div>
</template>
<script>
  export default {
    data(){
      return {
        msg:"Hello World"
      }
    }
  }
</script>
<style scoped>
  
</style>