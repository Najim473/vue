<template>
  <div>
    <button @click="hide = true">Hide</button>
    <h2>{{ msg }}</h2>
    <input
      type="text"
      placeholder="Coutinue"
      v-model="myComment"
      @click="handleClick"
      v-if="!hide"
    />
  </div>
</template>

<script>
export default {
  name: "theComponent",
  components: {},
  data() {
    return {
      msg: "The component",
      myComment: "",
      hide: false,
    };
  },
  methods: {
    handleClick(e) {
      this.$emit("update:modelValue", e.target.value);
    },
  },

  beforeCreate() {
    console.log("beforeCreate");
    console.log(this.msg);
  },
  created() {
    console.log("Created");
    console.log(this.msg);
  },
  beforeMount() {
    console.log("beforemount");
    console.log(this.msg);
  },
  mounted() {
    console.log("Mounted");
    console.log(this.msg);
  },
  beforeUpdate() {
    console.log("beforeupdate");
    console.log(this.msg);
  },
  updated() {
    console.log("updated");
    console.log(this.msg);
    alert('Are you sure for update !')
  },
  beforeUnmount() {
    console.log("beforeUnmount");
  },
  unmounted() {
    console.log("unmounted");
  },
};
</script>

<style lang="scss" scoped></style>
