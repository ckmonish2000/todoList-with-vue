<template>
  <div class="heading">
      <h2 class="title">Todo List</h2>
      <button class="reset" @click="reset"> reset</button>
  </div>
</template>


<script>
export default {
    name:"header",
    props:["set"],
    methods:{
        reset:function(){
            this.set.completed=false;
        }
    }
}
</script>

<style>
.heading{
    display: flex;
    flex-wrap: wrap;
    border-bottom: 2px grey groove;
    text-align: center;
}
.title{
    margin:10px;
}
.reset{
    padding: 5px;
    background: none;
    height: 35px;
    margin:10px;
    border:1px black double;

}

.reset:hover{
    box-shadow: 2px 2px black;
    transition: 0.5s;
}
</style>


