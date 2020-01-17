<template>
  <div id="app">
   <Data :set="todos"/>
   <Body class="bdy" :dta="todos"/>
  </div>
</template>

<script>
import Data from './components/header'
import Body from './components/body'

export default {
  name: 'app',
  components: {
    Data,
    Body
  },
  data(){
    return {
      todos:[
        {todoid:1,
        msg:"hello",
        completed:false
        },
         {todoid:2,
        msg:"hey",
        completed:false
        },
         {todoid:3,
        msg:"bye",
        completed:false
        }
      ]
    }
  }

}
</script>

<style>
*{
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: 'Roboto Mono', monospace;
  line-height: 1.4;
}
.bdy{
  width: 400px;
  margin:auto;
  margin-top:50px;
}
</style>
