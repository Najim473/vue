<template>
  <div>
    <h2>This is a popup</h2>
    <button @click="$emit('close','Popup close')">close popup</button>
  </div>
</template>
<script>
export default {
  name: "popup",
  emits: ["close"]
};
</script>

<style lang="scss" scoped></style>
