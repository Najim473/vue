<template>
  <div>
    <!-- v-html  -->
 <h3>What is your favorite kind of tacos?</h3>
 <!-- <p v-html="tacos"></p> -->
 <!-- v-text  -->
 <p v-text="tacos"></p>
 <p>{{tacos}}</p>
 <p><input v-model="tacos"></p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      // v-html 
      // tacos:`I like <a href="najimuddin.me" onclick="alert('I hacked you and stole all your tacos haha')">Al Pastor</a>`
      // tacos:`I like <a href="najimuddin.me">Al Pastor</a>`
      // v-text 
      tacos:'I like came asada'
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
