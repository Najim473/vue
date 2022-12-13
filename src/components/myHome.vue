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
    <button :class="[fruits ? activeClass : ' ']">submit</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      fruits: "",
      activeClass: "active",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
