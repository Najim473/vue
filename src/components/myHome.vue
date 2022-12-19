<template>
  <div class="main">
    <button @click="activeTab = 'TabA'">Tab A</button>
    <button @click="activeTab = 'TabB'">Tab B</button>
    <button @click="activeTab = 'TabC'">Tab C</button>
    <br />
    <br />
    <br />
    <keep-alive>
      <component :is="activeTab" />
    </keep-alive>
    <!-- <component :is="activeTab"/> -->
    <!-- <div class="tab">
      <TabA v-if="activeTab === 'TabA'" class="tabA" />
      <TabB v-if="activeTab === 'TabB'" class="tabB" />
      <TabC v-if="activeTab === 'TabC'" class="tabC" />
    </div> -->
  </div>
</template>
<script>
import TabA from "./TabA.vue";
import TabB from "./TabB.vue";
import TabC from "./TabC.vue";

export default {
  name: "myHome",
  components: {
    TabA,
    TabB,
    TabC,
  },
  data() {
    return {
      activeTab: "TabA",
    };
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
@import "./myHome.scss";
</style>
