<template>
  <h1>TODO App</h1>
    <input type="text" v-model="task" name="" id="i_field" placeholder="Add your new todo" >
    <button id="btn" @click="getInput">+</button><br>
</template>

<script>
import { defineComponent } from "@vue/runtime-core";
import "../assets/styling.css";

export default defineComponent({
    emits: ["addedTask"],
    data() {

        return{
            task: "",
            x: []
           
        }
    },
    methods:{
        getInput(){
        this.x.push(this.task)

        this.$emit('addedTask', this.x )

        this.task=""
        },
    },
});
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