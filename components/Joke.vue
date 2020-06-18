<template>
  <nuxt-link :to="'jokes/' + id">
    <div>
      <p class="joke-container">{{ joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: ["id", "joke"]
};
</script>

<style>
.joke-container {
  padding: 1rem;
  margin: 1rem;
  background: #f4f4f4;
}
</style>