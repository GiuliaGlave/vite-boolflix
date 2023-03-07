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
      <AppCardMovie />
      <AppCardTv />
    </div>
  </main>
</template>

<style lang="scss" scoped>
.row {
}
</style>
