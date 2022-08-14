<template>
  <div class="container">
    <DivMain @addedTask="addTask($event)"> </DivMain>
<div v-for="(task,index) in remainTasks" :key="index">
    <TaskRemain :remainingTasks="task"/>
</div>

  </div>
</template>

<script>
import DivMain from "./DivMain.vue"
import TaskRemain from './TaskRemain.vue';

import "../assets/styling.css"

export default {
  data(){
    return{
        remainTasks : []
        
    }
  },

  components:{
    DivMain,
    TaskRemain,

},
  methods:{
    addTask(tasks){
      console.log(tasks);
      this.remainTasks=[...tasks]
      
      console.log(this.remainTasks);
    }
  }
}
</script>

<style>
  
</style>