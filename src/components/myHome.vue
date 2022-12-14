<template>
<div>
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
  <br />
  <br />
  <br />
  <hr />
  <h2>Tip calculator</h2>
  <br>
  <p><strong>Total : {{customertotal}}</strong></p>
  <br>
<p>20% : {{tip20}}</p>
</div>
</template>
<script>
export default {
  data() {
    return {
      userData: "",
      counter: 0,
      customertotal:23.34
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
    tip20(){
      return (this.customertotal*.2).toFixed(2)
    }
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
