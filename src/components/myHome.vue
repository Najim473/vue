<script setup>
import { inject, ref } from "vue";
// import lists from './list.json'
// const state = reactive({ count: 0 });
const count = ref(0);
function increment() {
  count.value++;
}
</script>
<template>
  <div>
    <h2>Type Here:</h2>
    <textarea
      name="v-model"
      id=""
      cols="30"
      rows="10"
      v-model="message"
    ></textarea>
    <p>{{ message }}</p>
    <!-- <div>
  <input v-model="checkedNames" type="checkbox" value="paul"/>
  <label for="paul">paul</label>
  <input v-model="checkedNames" type="checkbox" value="Jhon"/>
  <label for="Jhon">Jhon</label>
  <h1>checked Name is : {{checkedNames}}</h1>
</div> -->
    <span class="v-model" v-for="option in options" :key="option">
   <div>
    <input v-model="checkedNames" type="checkbox" 
    :id="option.value"
    :value="option.value" />
      <label for="option.value">{{ option.value }}</label>
   </div>
    </span>
    <br />
    <br />
    <h1>checked Name is : {{ checkedNames }}</h1>
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: "Hello Bangladesh",
      checkedNames: [],
      options: [
        { value: "Jhon" },
        { value: "Paul" },
        { value: "George" },
        { value: "Ringo" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
