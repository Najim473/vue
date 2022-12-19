<template>
  <div class="main">
 <NameList>
  <template v-slot:default="slotProps">
    {{slotProps.firstName}}
    <br>
    <br>
    {{ slotProps.lastName }}
  </template>
 </NameList>
  </div>
</template>
<script>
import NameList from "./NameList.vue";
export default {
  name: "myHome",
  components: {
    NameList,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
@import "./myHome.scss";
</style>
