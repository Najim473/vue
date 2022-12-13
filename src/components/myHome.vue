<template>
  <div>
 <div class="item">
  <div class="quantity">
    <button class="incre" @click="counter>0 ? counter-=1:0">-</button>
    <span>count: {{counter}}</span>
    <button class="incre" @click=" counter+=1 ">+</button>

  </div>
 </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
     counter:0
    };
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
