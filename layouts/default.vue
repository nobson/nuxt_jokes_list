<template>
  <div class="container">
    <AppHeader />
    <nuxt />
  </div>
</template>

<script>
import AppHeader from "../components/AppHeader";

export default {
  components: {
    AppHeader
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  line-height: 1.6;
  background: #f4f4f4;
}

ul {
  list-style: none;
}

a {
  text-decoration: none;
}

.container {
  max-width: 800px;
  margin: 2rem auto;
  padding: 1rem 2rem;
  overflow: hidden;
  background: #fff;
}

h2 {
  margin: 0.3rem auto;
  padding: 0.3rem 2rem;
  overflow: hidden;
}
</style>
