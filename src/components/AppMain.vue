<script>
import AppCardMovie from "./AppCardMovie.vue";
import AppCardTv from "./AppCardTv.vue";

export default {
  data() {
    return {};
  },

  components: {
    AppCardMovie,
    AppCardTv,
  },
};
</script>

<template>
  <main class="bg-dark">
    <div class="container">
      <h2>Film</h2>
      <AppCardMovie />

      <h2 class="my-5">Serie TV</h2>
      <AppCardTv />
    </div>
  </main>
</template>

<style lang="scss" scoped>
main {
  color: white;
}
</style>
