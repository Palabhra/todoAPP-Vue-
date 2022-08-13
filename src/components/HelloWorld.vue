<template>
  <div class="container">
    <h1>tasks:  {{this.remainTasks}}</h1>
    <DivMain @addedTask="addTask($event)"> </DivMain>

    <TaskRemain/>
  </div>
</template>

<script>
import DivMain from "./DivMain.vue"
import TaskRemain from './TaskRemain.vue';

import "../assets/styling.css"

export default {
  data(){
    return{
        remainTasks : ""
        
    }
  },

  components:{
    DivMain,
    TaskRemain,

},
  methods:{
    addTask(tasks){
      
      this.remainTasks=[]
      this.remainTasks.push(tasks)
      
      console.log(this.remainTasks.target);
    }
  }
}
</script>

<style>
  
</style>