<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <p>父组件数据->{{num}}</p>
    <Content :num="num" :name="uname" v-on:add="addEvent" v-on:reduct="reduction"></Content>
  </div>
</template>

<script>
import Content from './content.vue'

export default {
  name: 'HelloWorld',
  data () {
    return {
      num:10,
      msg: 'Welcome to Your Vue.js App',
      uname:'我是父组件传递过来的数据'
    }
  },
  methods:{
    addEvent(msg){
      console.log(msg);
      this.num++;
    },
    reduction(msg){
      console.log(msg);
      this.num--;
    }
  },
  components:{
    Content
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
