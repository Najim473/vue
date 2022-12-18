<template>
  <div className="flex">
    <myHome />
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
