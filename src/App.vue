<script>
import axios from "axios";
import { store } from "./data/store";

import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
  data() {
    return {
      store,
      /* API */
      base_url: "https://api.themoviedb.org/3",
      api_key: "350db113e3f2ef04d5a23ed8840c1433",
      /* {{base_url}}{{api_key}}return */
      /* HEADER */
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
    fetchMovie(query) {
      axios
        .get(
          `${this.base_url}/search/movie?api_key=${this.api_key}&query=${query}`
        )
        .then((response) => {
          store.movieList = response.data.results;
          console.log(this.movieList);
        });
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
    @newSearch="fetchMovie"
  />
  <AppMain />
</template>

<style lang="scss"></style>
