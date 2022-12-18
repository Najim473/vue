<template>
  <div>
    <p>Article</p>
    <h2>Title is : {{ title }}</h2>
    <h2>Likes : {{ like }}</h2>
    <h2>Published : {{isPublished ? 'Yes':'No'}}</h2>
  </div>
</template>

<script>
export default {
  name: "Article",
  props: {
    title: {
        type:String,
        required:true,
        default:"This is default value"
    },
    like: Number,
    isPublished: Boolean,
  },
};
</script>

<style lang="scss" scoped></style>
