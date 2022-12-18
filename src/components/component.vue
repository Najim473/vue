<template>
  <div>
    <p class="paragraph">
      I like to eat {{name}} also like to eat {{name2}}
    </p>
  </div>
</template>
<script>
export default {
  name: "component",
  props:['name','name2']
};
</script>

<style lang="scss" scoped>
@import './component.scss'
</style>
