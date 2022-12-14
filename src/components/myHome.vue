<template>
  <form @submit.prevent="submitForm">
    <div>
      <label for="name">Name:</label>
      <br />
      <input type="text" id="name" v-model="name" required />
    </div>
    <div>
      <label for="email">Email:</label>
      <br />
      <input type="email" id="email" v-model="email" required />
    </div>
    <div>
      <label for="caps">HOW DO I TURN OFF CAPS LOCK</label>
      <textarea
        id="caps"
        cols="30"
        rows="10"
        v-model="caps"
        required
      ></textarea>
    </div>
    <button :class="[name ? activeClass : '']" type="submit">submit</button>
    <div>
      <h5>Response from server:</h5>
      <pre>{{ response }}</pre>
    </div>
  </form>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      caps: "",
      response: "",
      activeClass: "active",
    };
  },
  methods: {
    submitForm() {
      axios
        .post("https://jsonplaceholder.typicode.com/posts", {
          name: this.name,
          email: this.email,
          caps: this.caps,
        })
        .then((response) => {
          this.response = JSON.stringify(response, null, 2);
        })
        .catch((error) => {
          this.response = "Error:" + error.response.status;
        });
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
