<template>
  <div class="hello">
    <h3>{{name}}</h3>
    <button @click="reduction" type="button">-</button>
    <button @click="add" type="button">+</button>
    <p>{{n}}</p>
  </div>
</template>

<script>
export default {
  props:['num','name'],
  name: 'Content',
  data () {
    return {
      n:0
    }
  },
  mounted(){
    this.n=this.num;
  },
  methods:{
    reduction(){
      this.n--;
      this.$emit('reduct','我是子组件传递过去的数据');
    },
    add(){
      this.n++;
      this.$emit('add','我是子组件传递过去的数据');
    }
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
