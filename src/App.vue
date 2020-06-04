<template>
  <div id="app">
    <!-- <p v-show="toggle">
      Hello ERA
    </p>
    <p>
      <helloConponent></helloConponent>
    </p> -->
    
    <!-- <p v-else>

    </p> -->
    <p>信号機の色を変える</p>
    <button v-on:click="onClick">変えちゃうぞ</button>
    <br>
    <br>
    <!-- <p>{{colors}}</p> -->
    <p>信号機の色は……</p>
    <p v-if="color==='red'" style="color:red;background-color:black">
      赤やで！Stop
    </p>
    <p v-else-if="color==='yellow'" style="color:yellow; background-color:black">
      黄色です！Caution
    </p>
    <p v-else-if="color==='green'" style="color:green; background-color:black">
      青じゃん！Go
    </p>
    <p v-else>
      故障中
    </p>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      // toggle:false 
      colors: ['red','yellow','green'],
      color: null,
      i:0
    }
  },
  methods:{
    onClick(){
      this.color = this.colors[this.i]
      if (this.i<3){this.i ++}
      else{this.i=0}
    }
  }
  // components:{
  //   helloConponent:{template:'<p>Hello</p>'}
  // }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
