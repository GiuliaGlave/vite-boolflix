<script>
import axios from "axios";
import { store } from "./data/store";

import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
  data() {
    return {
      store,
    };
  },

  components: {
    AppHeader,
    AppMain,
  },

  created() {
    /* axios.get("movie-list").then((response) => {});
    axios.get("tv-list").then((response) => {}); */
  },
};
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss"></style>
