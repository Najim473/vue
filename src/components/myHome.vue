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
    <h2>What is your favorite fruits:</h2>
    <textarea id="" cols="30" rows="3" v-model="fruits"></textarea>
    <!-- <button v-if="fruits" type="submit">submit</button> -->
    <button v-show="fruits" type="submit">submit</button>
  </div>
  <div>
    <h3>Do You like Fruits</h3>
    <br>
    <input type="radio" v-model="fruits" value="yes" id="yes">
    <label for="yes"> Yes</label>
    <br>
    <br>
    <input type="radio" v-model="fruits" value="no" id="no">
    <label for="no"> No</label>
    <br>
    <br>
    <br>
    <p v-if="fruits === 'yes'" class="thumbs">😄</p>
    <p v-else-if="fruits === 'no'" class="thumbs">😧</p>

  </div>
</template>
<script>
export default {
  data() {
    return {
      fruits: ''
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
