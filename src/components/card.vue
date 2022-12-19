<template>
  <div>
    <div class="card">
      <div id="card-header">
        <slot name="header"></slot>
      </div>
      <div id="card-content">
        <slot></slot>
      </div>
      <div id="card-footer">
        <slot name="footer"></slot>
      </div>
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
  box-shadow: 3px 3px 2px 0px rgb(161, 163, 169);
  padding: 16px;
  transition: 1s;
}
.card:hover {
  box-shadow: 23px 3px 2px 0px rgb(54, 125, 23);
}
</style>
