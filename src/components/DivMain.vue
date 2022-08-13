<template>
  <h1>TODO App</h1>
    <input type="text" v-model="task" name="" id="i_field" placeholder="Add your new todo" >
    <button id="btn" @click="getInput">+</button><br>
</template>

<script>
import "../assets/styling.css";

export default {
    emits: ["addedTask"],
    data() {
        return{
            task: "",
            x: [{id: 1,value: "Hi I'm data"}]
           
        };
    },
    methods:{
        getInput(){
       
       

        this.x.push(this.task)
         console.log(this.x);
        this.$emit('addedTask', this.x )

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