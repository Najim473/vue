<script setup>
import { inject, ref } from "vue";
// import lists from './list.json'
// const state = reactive({ count: 0 });
const count = ref(0)
function increment() {
   count.value++ ;
}
</script>
<template>
  <div>
  <p>{{message}}</p>
   <ul>
    <li v-for="(item) in items">{{item}}</li>
   </ul>
  </div>
</template>
<script>
 export default {
  name:'app',
  data(){
    return{
      message:'Hello World',
      items:[
        'Mango',
        'Apple',
        'Orange',
        'Banana'
      ]
    }
  }
 }
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
