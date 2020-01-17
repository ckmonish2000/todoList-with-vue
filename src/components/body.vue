<template>
  <div class="bodyparent">
    <div v-for="x in dta" :key="x.id">
<Item :itm="x" v-on:delete-todo="$emit('deletes',x.todoid)"/>
    </div>
  </div>
</template>

<script>
import Item from "./items"
export default {
    name:"body",
    props:["dta"],
    components:{
        Item
    }

}
</script>

<style>
.bodyparent{
    background: grey;
    color:white;
    text-align: center;
    border:3px black solid;
}
</style>