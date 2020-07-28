<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="ceshi">文字</div>
    <el-button @click="increment">默认按钮</el-button>
  </div>
</template>

<script>
import {configUrl} from './js/configUrl'
import{mapGetters,mapActions} from 'vuex'
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  created(){
    console.log(configUrl)
  },
  methods:{
    ...mapActions(['increment','reduce','resumeList','dataAppId']),
    ...mapGetters(['count']),
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" rel="stylesheet/less" scoped>
@import "css/style.less";
.ceshi{
  color: @color;
}
</style>
