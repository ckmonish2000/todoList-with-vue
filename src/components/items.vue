<template>
  <div class="itemp" :class="{'iscmp':itm.completed}">
<h2>{{itm.msg}}</h2>
<input type="checkbox" @change="mx" class="inp">
<button class="del" @click="$emit('delete-todo',itm.todoid)">x</button>

  </div>
</template>

<script>
export default {
    name:'items',
    props:["itm"],
    methods:{
        mx:function(){
            this.itm.completed=!this.itm.completed;
        }
    }
}
</script>

<style>
.itemp{
    background: #4d4646;
    border-bottom:white 2px solid;
    padding: 5px;
    color: white;
    display: flex;
    flex-wrap: wrap;
    justify-content: center
}
.itemp:hover{
    background: white;
    color:#4d4646;
    transition: 0.3s;
}
.iscmp{
    text-decoration: line-through;
}
.inp{
    margin:10px;
}

.del{
    background: red;
    color:white;
    border-radius:100px;
    padding: 5px;
    position: relative;
    left: 30%;
    text-decoration: none;
    
}
.del:hover{
    color: red;
    background: white;
    box-shadow: 3px 3px 3px black;
    transition: 0.3s;
}
</style>