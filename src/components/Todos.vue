
<script>
import Todo from '../components/Todo.vue'
export default{
name:'Todos',
components:
{
Todo
},
props:[
    "ss"
],
// methods:{
//     callme(){
//         console.log(this.ss.id);
//     }
// }
}
</script>

<template>
<div id="Todos">
<ul>
    <li v-bind:key="item.id" v-for="item in ss">
    <Todo v-bind:rrr="item"  v-on:todos-delete-todo="$emit('deleteme', item.id)" ></Todo> 
    </li>
</ul>
</div>
</template>

<style>
</style>