<template>
  <h1>
    Fruits Name:
    <input type="text" v-model.lazy="userData" />
  </h1>
  <h2 v-if="userData">Initial entry: {{ userData }}</h2>
  <h2 v-if="userData">Computed value: {{ greeting }}</h2>
  <br />
  <br />
  <br />
  <hr />
  <p>counter : {{counter}}</p>
  <p>counter computed : {{countupComp}}</p>
  <button @click="countUp">Increase</button>
</template>
<script>
export default {
  data() {
    return {
      userData: "",
      counter: 0,
    };
  },
  methods: {
    countUp() {
      this.counter++;
    },
  },
  computed: {
    greeting() {
      return `Do you like ${this.userData}`;
    },
    countupComp() {
      return this.counter + 1;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
