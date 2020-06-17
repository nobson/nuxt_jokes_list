<template>
  <div>
    <h1>About DadJokes</h1>
    <p>This is THE site about fine dad jokes.</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "About dad jokes",
      meta: [
        {
          hid: "description",
          name: "content",
          content: "Best place for corny dad jokes."
        }
      ]
    };
  }
};
</script>

<style>
</style>