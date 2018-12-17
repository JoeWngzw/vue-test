<template>
  <div id="app">
    <!--<button :class = "num == i? 'active' : ''" @click="change(i)" v-for="(o,i) in btlist">{{o}}-->

      <!--<div :class ="num == i ? 'active' : ''">我是{{o}}</div>-->
    <!--</button>-->

    <HelloWorld msg="Welcome to Your Vue.js App" sayhi="hello joe"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
      HelloWorld
  },
    data(){
      return{
          btlist:['新闻','衣服','柜子'],
					num:1,

      }
    },
    methods:{
        change(i){
            this.num = i;

        }
    }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#app button.active{
  background-color: aquamarine;
  position: relative;
}


  #app button div{
    width: 200px;
    height: 200px;
    border: 1px solid #ccc;
    position: absolute;
    display: none;
  }

#app button div.active{
    display: block;
}


</style>
