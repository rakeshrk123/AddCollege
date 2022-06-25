<script>

export default{
name:'Todo',
props:[
    "rrr"
],
methods:{

deleteCollege(){
  
  this.$emit('todos-delete-todo',this.rrr.id)
}
}
}

</script>
<template>
<div id="Todo">
<p>{{rrr.subject}}</p>
<p>{{rrr.marks}}</p>
<button @click="deleteCollege">Delete</button>
</div>
</template>

<style>


</style>