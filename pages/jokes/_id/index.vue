<template>
  <div>
    <nuxt-link to="/jokes">Back to Jokes</nuxt-link>
    <p class="joke-container">{{ joke }}</p>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      joke: {}
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data.joke;
    } catch (err) {
      console.log(err);
    }
  }
};
</script>

<style>
.joke-container {
  padding: 1rem;
  margin: 1rem;
  background: #f4f4f4;
}
</style>