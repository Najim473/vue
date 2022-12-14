<template>
  <div
    class="box"
    @mousemove="xcoordinate"
    :style="{ backgroundColor: `hsl(${x},80%,50%)` }"
  >
    <button @click="increment">increment</button>
    <button @click="decrement">decrement</button>
    <p>{{ counter }}</p>

    <br />
    <p>Pixels across {{ x }}</p>
  </div>

  <div>
    <ul>
      <li v-for="comment in comments" :key="comment">{{ comment }}</li>
    </ul>
    <br />
    <input
      @keyup.enter="addComment"
      v-model="newComment"
      placeholder="Add a comment"
    />
  </div>
</template>
<script>
export default {
  data() {
    return {
      counter: 0,
      x: 0,
      newComment: '',
      comments: ["Looks great you!", "I love to sea", "Where are you at"],
    };
  },
  methods: {
    increment() {
      this.counter++;
    },
    decrement() {
      this.counter--;
    },
    xcoordinate(e) {
      this.x = e.clientX;
    },
    addComment() {
      this.comments.push(this.newComment);
      this.newComment = "";
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
