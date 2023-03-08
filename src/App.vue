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
    fetchResults(query) {
      this.fetchMovie(query);
      this.fetchTVSeries(query);
    },
    fetchMovie(query) {
      axios
        .get(
          `${this.base_url}/search/movie?api_key=${this.api_key}&query=${query}`
        )
        .then((response) => {
          store.movieList = response.data.results;
        });
    },
    fetchTVSeries(query) {
      axios
        .get(
          `${this.base_url}/search/tv?api_key=${this.api_key}&query=${query}`
        )
        .then((response) => {
          store.tvShowList = response.data.results;
          console.log(this.tvShowList);
        });
    },
  },
};
</script>

<template>
  <AppHeader
    :name="appName"
    :placeholder="searchPlaceholder"
    :search="searchButton"
    @newSearch="fetchResults"
  />
  <AppMain />
</template>

<style lang="scss">
body {
  background-color: #222;
}
</style>
