<template>
  <div class="main">
 <button @click="getTaco">Click to order a taco</button>
 <br>
 <br>
 <br>
 <h2>{{orderStatus}}</h2>
 <p v-if="orderSubmitted">{{orderSubmitted}}</p>
  </div>
</template>
<script>
export default {
  data() {
    return {
  orderStatus:'Where is taco...',
  orderSubmitted:null
    };
  },  
  methods:{
    getTaco(){
      this.orderStatus = '🌮!'
    }
  },
  watch: {
   orderStatus(newValue,oldValue){
this.orderSubmitted = 'your order was submitted !'
setTimeout(() => this.orderSubmitted=null,1000);
   }
  },
};
</script>
<style lang="scss" scoped>
@import "./myHome.scss";
</style>

