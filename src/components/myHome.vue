<template>
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
<script setup>
import { ref } from "vue";
// const state = reactive({ count: 0 });
const count = ref(0)
function increment() {
   count.value++ ;
}
</script>
<style lang="scss" scoped>
@import "./myHome.scss";
</style>
