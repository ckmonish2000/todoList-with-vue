<template>
  <div class="heading">
      <h2 class="title">Todo List</h2>
      <div class="adds">
      <input type="text" class="add" v-model="todo" placeholder="add todos...">
      <button class="reset" @click="adds">submit</button>
      </div>
  </div>
</template>


<script>
export default {
    name:"header",
    props:["set"],
    data(){
        return{
            tool:"",
            Id:0
        }
    },
    methods:{
        adds:function(e){
            e.preventDefault();
            const newtodo={
                id: this.Id+1,
                title:this.tool
            }
            this.Id=this.Id+1;
            this.$emit("add-new",newtodo)


        }
    }
    }

</script>

<style>
.heading{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
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
.add{
    height: 30px;
    margin-top: auto;
    margin-left:auto;
    margin-bottom: auto;
    width: 400px;
    
}

</style>


