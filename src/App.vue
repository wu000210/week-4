<template>
  <div id="app">
    <el-button type="primary" @click="openDiag = ture">Primary</el-button>
    <el-dialog :visible="openDiag">
    <div>
    <input type="text" v-model="sendTreat" />
    </div>
    <HelloWorld msg="My first App"/>
    <MyFirst :treat="sendTreat"/>
    </el-dialog>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import MyFirst from './components/MyFirst.vue';

export default {
  name: 'app',
  components: {
    HelloWorld,
    MyFirst 
  },
  data: function() {
    return {
      sendTreat: "Raw Hide",
      openDiag: false
    };
  }  
};
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
</style>
