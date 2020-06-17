<template>
  <div>
    <h2>Jokes</h2>
    <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke" />
  </div>
</template>

<script>
import axios from "axios";
import Joke from "../../components/Joke";

export default {
  components: {
    Joke
  },
  data() {
    return {
      jokes: []
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get("https://icanhazdadjoke.com/search", config);
      this.jokes = res.data.results;
    } catch (err) {
      console.log(err);
    }
  }
};
</script>

<style>
</style>