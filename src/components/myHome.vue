<template>
  <div>
      <p v-for="(joke, key, index) in jokes" :key="joke">
        {{index}} - <span>:</span> 
        {{key}} {{joke}}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      jokes: {
        question: "What did one baby prototype say to the other?",
        answer: `I'll race you to class!`,
        response: "groan",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
