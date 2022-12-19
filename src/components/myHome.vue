<template>
  <div class="main">
    <!-- <card content="content 01"/>
    <card content="content 02"/> -->
    <card/>
    <card>Card content</card>
    <card><h2>Card content</h2></card>
    <card>
      <img
        src="https://i.ibb.co/zRj6zwP/pexels-anna-shvets-4588065.jpg"
        alt=""
      />
    </card>
    <!-- NAMED SLOTS  -->
 <card>
  <template v-slot:header>
    Header
  </template>
  <template v-slot:default>
    <img src="https://i.ibb.co/3hcHzsg/pexels-kelvin-valerio-617278.jpg" alt="">
  </template>
  <template v-slot:footer>
    <button>View details</button>
  </template>

 </card>
  </div>
</template>
<script>
import card from "./card.vue";
export default {
  name: "myHome",
  components: {
    card,
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
