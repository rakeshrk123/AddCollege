<template>
<div id="app">
<Todos  v-on:deleteme="deleteok" v-bind:ss="college"></Todos>
<CLG v-on:college_new="getcollege" ></CLG>
</div>
</template>

<script>
import Todos from './components/Todos.vue'
import CLG from './components/AddCollege.vue'

export default {
  name: 'app',
  components: {
    Todos,
    CLG
  },
  data() {
    return {
      college: [
        {
          id: 1,
          subject: "English",
          marks: "40"
        },
        {
          id: 2,
          subject: "Marathi",
          marks: "50"
        }
      ]
    }
  },
  methods:{
getcollege(newobj)
{
  this.college=[...this.college , newobj]
},

deleteok(id)
{
  this.college = this.college.filter((element, index) =>  {
          return  element.id !== id
        }
  )
}
}

}

</script>


<style>

</style>
