<template>
  <div class="hello">
  {{as}}
      <template v-if="aa">
        我时条件为true看到的
        <p>你是一头猪</p>
      </template>
      <template v-else>
        我是条件为false看到的
        <p>你是两头猪</p>
      </template>
      <ul>
        <li v-for="(tiem,index) in arr">{{tiem}}-{{index}}</li>
      </ul>
      <ul>
        <li v-for="(item,index) in user" v-bind:key="index">
          <span>{{item.name}}</span>
          <span>{{item.age}}岁</span>
          {{index}}
        </li>
      </ul>
      <button @click="han">切换</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      hello:'hello,Vue!!!',
      as:'你是猪',
      aa:true,
      arr:['张三','李四','王五'],
      user:[
        {
          id:0,
          name:'李白',
          age:20
        },{
          id:1,
          name:'韩信',
          age:21
        },{
          id:2,
          name:'花木兰',
          age:19
        }
      ]
    }
  },
  methods:{
    han(){
      this.aa=!this.aa;
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
