<template>
  <div>
    <h1>What is your favorite fruits</h1>
    <p><input v-model="fruits" /></p>
    <p v-once="fruits">{{ fruits }}</p>
    <span v-pre>My favorite fruits is {{ fruits }}</span>
    <pre>{{ $data }}</pre>
  </div>
</template>
<script>
export default {
  data() {
    return {
      fruits: "I like to eat Apple",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
