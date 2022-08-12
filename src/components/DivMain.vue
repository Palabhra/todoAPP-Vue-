<template>
  <h1>TODO App</h1>
    <input type="text" v-model="task" name="" id="i_field" placeholder="Add your new todo" >
    <button id="btn" @click="getInput">+</button><br>
        <div class="taskContainer">
          
        </div>
    <br><h3>You have [] pending tasks</h3>
</template>

<script>
import "../assets/styling.css";

export default {
    data() {
        return{
            task: "",
           
        };
    },
    methods:{
        getInput(x){
        console.log(this.task);
         
        x = this.task
        this.$emit('addedTask', x )
        this.task=""
        },
    },
};
</script>
<style scoped>
h1{
    padding-top: 5%;
    text-align: left;
    margin-left: 10%;
}
h3{
    text-align: left;
    margin-left: 10%;
    font-weight:200;
}
</style>