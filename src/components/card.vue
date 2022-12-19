<template>
  <div>
    <div class="card">
      <!-- {{ content }} -->
      <slot>Defalut content</slot>
    </div>
  </div>
</template>
<script>
export default {
  name: "card",
  // props: ["content"],
};
</script>

<style scoped>
.card {
  box-shadow: 3px 3px 2px 0px rgb(23, 57, 125);
  padding: 16px;
  transition: 1s;
}
.card:hover {
  box-shadow: 23px 3px 2px 0px rgb(54, 125, 23);
}
</style>
