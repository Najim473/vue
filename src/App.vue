<template>
  <div className="flex">
    <myHome name="Mango"/>
    <!-- <mySelf/>     -->
  </div>
</template>
<script>
import myHome from "./components/myHome.vue";
export default {
  name: "App",
  components: {
    myHome,
  },
};
</script>
