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
  <AppCardMovie />
  <AppCardTv />
</template>

<style lang="scss" scoped></style>
