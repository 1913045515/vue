<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>我是测试页面</h2>
    <div id="app">
         <span v-bind:title="message">
            鼠标悬停几秒钟查看此处动态绑定的提示信息！
        </span>
    </div>

    <div id="app-3">
        <p v-if="seen">现在你看到我了</p>
    </div>

  <div>
      <ol>
          <li v-for="person in persons">
                {{person.name}}
          </li>
      </ol>
  </div>
    <p>{{funcMsg}}</p>
    <button v-on:click="clickFunc">点击事件</button>
    <p>{{modelMsg}}</p>
    <input v-model="modelMsg">
      <div id="example">
        <my-component></my-component>
      </div>
  </div>
</template>
<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "欢迎进入vue的世界",
      message: '页面加载于 ' + new Date().toLocaleString(),
      seen:true,
      visible: false,
      modelMsg:"我是初始值！！！",
      funcMsg:"初始值",
      persons:[
          {name:'linzhiqiang'},
          {name:'zhaotong'},
          {name:'zhangxiang'}
      ]
    };
  },
  methods:{
     clickFunc:function(){
        this.funcMsg="aaaaaaaaaaaa"
     }
  }
};
</script>

<style scoped>
h1,
h2 {
  font-weight: normal;
  color: #42b983;
}
</style>
