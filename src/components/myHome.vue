<template>
  <div class="main">
   
    <theComponent/>
  </div>
</template>
<script>
import theComponent from "./TheComponent.vue";
export default {
  name: "myHome",
  components: {
    theComponent,
  },
  data() {
    return {
      // msg: "vue js 3 lifecycle hooks",
      // myComment: "",
    };
  },
  methods: {
    // handleClick() {
    //   console.log("Clicked");
    },
  // },
  // beforeCreate() {
  //   console.log("beforeCreate");
  //   // console.log(this.msg);
  // },
  // created() {
  //   console.log("Created");
  //   // console.log(this.msg);
  // },
  // beforeMount() {
  //   console.log("beforemount");
  //   // console.log(this.msg)
  // },
  // mounted() {
  //   console.log("Mounted");
  //   // console.log(this.msg)
  // },
  // beforeUpdate() {
  //   console.log("beforeupdate");
  // },
  // updated() {
  //   console.log("updated");
  // },
};
</script>
<style lang="scss" scoped>
@import "./myHome.scss";
</style>
