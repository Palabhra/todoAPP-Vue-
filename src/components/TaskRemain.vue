<template>
  <h3>{{remainTask()}}</h3>
</template>

<script>

export default {
  data() {
    return {
      printRemainTask: "World"
    }
  },
  props: {
    remainingTasks: String
    },
    methods: {
      remainTask(){
        
        
        console.log(this.printRemainTask);
      }
    },

}
</script>

<style>
    
</style>