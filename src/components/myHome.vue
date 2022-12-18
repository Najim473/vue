
<!-- BEER COUNTING  -->
<template>
 <div v-for="beer in beers">
  <h1>{{beer.name}} </h1>
 </div>
</template>
<script>
export default {
  data() {
    return {
      bottom: false,
      beers: []
    };
  },
  watch: {
    bottom(newValue) {
      if (newValue) {
        this.addBeer();
      }
    }
  },
  created() {
    window.addEventListener("scroll", () => {
      this.bottom = this.bottomVisible();
    });
    this.addBeer();
  },
  methods: {
    bottomVisible() {
      const scrollY = window.scrollY;
      const visible = document.documentElement.clientHeight;
      const pageHeight = document.documentElement.scrollHeight;
      const bottomOfPage = visible + scrollY >= pageHeight;
      return bottomOfPage || pageHeight < visible;
    },
    addBeer() {
      axios.get("https://api.punkapi.com/v2/beers/random").then((response) => {
        let api = response.data[0];
        let apiInfo = {
          name: api.name,
          desc: api.description,
          img: api.image_url,
          tips: api.brewers_tips,
          tagline: api.tagline,
          food: api.food_pairing
        };
        this.beers.push(apiInfo);
        if (this.bottomVisible()) {
          this.addBeer();
        }
      });
    }
  }
};
</script>
<style lang="scss" scoped>
@import "./myHome.scss";
</style>

<!-- COUNTING WATCHER CHANGE  -->
<!-- <template>
  <div>
    <input type="number" v-model.number="counter" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      counter: 0,
      bottom: false,
      beers: [],
    };
  },  
  watch: {
    counter(newvalue, oldValue) {
      console.log(
        `The counter has changed! It was old ${oldValue} and It's new value ${newvalue}`
      );
    },
  },
};
</script> -->