<script setup>
import { ref } from "vue";
import lists from './list.json'
// const state = reactive({ count: 0 });
const count = ref(0)
function increment() {
   count.value++ ;
}
</script>
<template>
<ul class="list ">
<li class="listItem" v-for="list in lists">
{{list.title}}
</li>
</ul>
  <Nav>
    <ul>
      <li>Home</li>
      <li>About</li>
      <li>Service</li>
      <li>Contact</li>
    </ul>
  </Nav>
  <button class="btn" @click="increment">{{count}}</button>
 <div>
  <h3>What is your favorite kind of taco?</h3>
    <input v-model="tacos"/>
    <!-- <p v-once="tacos">{{tacos}}</p> -->
    <p>{{tacos}}</p>
    <pre>
      {{$data}} 
    </pre>
 </div>
  </template>
<script>
 export default {
  name:'app',
  data(){
    return{
      tacos:'I like Al pastor tacos'
    }
  }
 }
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
