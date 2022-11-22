<template>
  <!-- <myButton @click="handleClick"/> -->
  <myButton @buttonClicked="showAlert" text="My button text" />
  <h1 @click="handleClick">Hello {{ name }}</h1>
</template>
<script setup>
import { ref } from "vue";
import myButton from ".././src/components/button/button.vue";
const name = ref("Vue js");
const handleClick = () => {
  name.value = "Vue";
};
const showAlert = newName => {
  // alert("Child button was clicked");
  name.value = newName
};
</script>
<!-- <script>
import myButton from '.././src/components/button/button.vue'
 import {ref} from 'vue'
 export default{
  setup(){
    const name = ref(" Vue js")
    const handleClick =()=>{
      name.value = 'Vue';
    }
    const showAlert=()=>{
      alert('Child button was clicked')
    }
    return{
      name,
      handleClick,
      showAlert
    }
  },
  components:{
    myButton
  }
 }
</script> -->
