<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    
  </div>
</template>

<script>
import Jsonob from './index.js'
export default {
  data () {
    return {
      msg: 'Welcome'
    }
  },
  mounted(){
    let cb=(newv,oldv)=>{
      alert('新值：' + newv + '----' + '旧值：' + oldv)
    }
    let data = {
      a:200,
      l1:{
        b:'str',
        c:[1,2,3,],
        l2:{
          d:90
        }
      }
    }
    let j = new Jsonob(data,cb)
    console.log(j)
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
