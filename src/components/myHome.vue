<template>
  <div class="row">
    <input v-model.number="num1" type="number" />
    <span>+</span>
    <input v-model.number="num2" type="number" />
    <span>=</span>
    <span>{{ num1 + num2 }}</span>
  </div>
  <div class="row second">
    <select v-model="name">
      <option>Apple</option>
      <option>Orange</option>
      <option>Mango</option>
      <option>Lemon</option>
      <option>Banana</option>
    </select>
    <br />
    <p v-if="name">My favorite fruit is {{ name }}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      name: "",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
