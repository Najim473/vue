<template>
  <br />
  <br />
  <h3>Search a Title : <input v-model="filterText" /></h3>
  <br />
  <br />
  <h3>
    Sort titles by:
    <button @click="sortLowest">Lowest Rated</button>
    <button @click="sortHighest">Highest Rated</button>
  </h3>

  <table>
    <thead>
      <tr>
        <th v-for="key in columns">
          {{ key }}
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="entry in filtredFilms">
        <td v-for="key in columns">
          {{ entry[key] }}
        </td>
      </tr>
    </tbody>
  </table>
</template>
<script>
export default {
  data() {
    return {
      columns: ["title", "rating"],
      ratingsInfo: [
        { title: "White Chicks", rating: 82 },
        { title: `Grey's anatomy`, rating: 98 },
        { title: "Person Break", rating: 93 },
        { title: "How I Net Your Mother", rating: 94 },
        { title: "Supernatural", rating: 85 },
        { title: "Breaking Bed", rating: 91 },
        { title: "Death Note", rating: 97 },
        { title: "Naruto", rating: 83 },
      ],
      filterText: ''
    };
  },
  methods: {
    sortLowest() {
      this.ratingsInfo.sort((a, b) => (a.rating > b.rating ? 1 : -1));
    },
    sortHighest() {
      this.ratingsInfo.sort((a, b) => (a.rating < b.rating ? 1 : -1));
    },
  },
  computed: {
    filtredFilms() {
      let filter = new RegExp(this.filterText, 'i');
      return this.ratingsInfo.filter((el) => el.title.match(filter));
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./myHome.scss";
</style>
