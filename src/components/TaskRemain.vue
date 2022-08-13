<template>
        <div class="taskContainer">
          <h4>Hello world</h4>
        </div>
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