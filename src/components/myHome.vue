<template>
  <div class="main">
    <button @click="showPopup=true">Show Popup</button>
    <Popup v-show="showPopup" @close="closePopup"/>
  </div>
</template>
<script>
import Popup from "./popup.vue";
export default {
  name: "myHome",
  components: {
    Popup,
  },
  data() {
    return {
      showPopup:false
    };
  },
  methods:{
    closePopup(name){
      this.showPopup=false
      console.log('name',name);
    }
  }
};
</script>
<style lang="scss" scoped>
@import "./myHome.scss";
</style>
