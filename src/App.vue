<template>
  <div id="app">
   <Data :set="todos" @add-new="addTodos"/>
   <Body class="bdy" :dta="todos" v-on:deletes="hello"/>
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
  },
  methods:{
    hello(todoid){
      this.todos=this.todos.filter(todo=>todo.todoid!=todoid)
    },
    addTodos(newtodo){
      this.todos.push(newtodo)
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
