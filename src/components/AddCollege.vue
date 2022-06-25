<script>

import { v4 as uuidv4 } from 'uuid';
export default {
    name: 'AddCollege',
    data() {
        return {
            id: "",
            subject: "",
            marks: ""
        }
    },
    methods:{
     addCollege(event){
    event.preventDefault();
    const newCollegeobj={
    id:uuidv4 (),
    subject:this.subject,
    marks:this.marks
    }
    this.$emit("college_new",newCollegeobj);
    } 
      

    }
}
</script>
<template>
<div id="AddCollege">
<form @submit="addCollege">
<input type="text" v-model="subject" name="subject" />
<input type="text" v-model="marks" name="marks" />
<button type="submit">Add</button>
</form>

</div>
</template>

<style>
</style>