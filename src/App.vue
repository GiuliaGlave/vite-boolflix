<script>
import axios from "axios";
import { store } from "./data/store";

import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
  data() {
    return {
      store,
      appName: "BOOLFLIX",
      searchPlaceholder: "Cerca film o serie TV ",
      searchButton: "search",
    };
  },

  components: {
    AppHeader,
    AppMain,
  },

  methods: {
    do_something(param) {
      console.log(param);
    },
  },

  created() {
    /* axios.get("movie-list").then((response) => {});
    axios.get("tv-list").then((response) => {}); */
  },
};
</script>

<template>
  <AppHeader
    :name="appName"
    :placeholder="searchPlaceholder"
    :search="searchButton"
    @newSearch="do_something"
  />
  <AppMain />
</template>

<style lang="scss"></style>
