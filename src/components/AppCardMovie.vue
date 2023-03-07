<script>
import { store } from "../data/store";
export default {
  data() {
    return {
      store,
    };
  },
  methods: {
    getFlag(country) {
      country = country.toUpperCase();
      //ci molte bandiere non corrispondono alla lingua perchè il codice del paese è diverso dal codice ISO
      if (country == "EN") return "https://flagsapi.com/GB/flat/64.png";
      if (country == "EL") return "https://flagsapi.com/GR/flat/64.png";
      if (country == "DA") return "https://flagsapi.com/DK/flat/64.png";
      if (country == "KO") return "https://flagsapi.com/KR/flat/64.png";
      if (country == "FA") return "https://flagsapi.com/IR/flat/64.png";
      if (country == "JA") return "https://flagsapi.com/JP/flat/64.png";
      if (country == "ZH") return "https://flagsapi.com/CN/flat/64.png";
      if (country == "AR") return "https://flagsapi.com/EG/flat/64.png";
      return "https://flagsapi.com/" + country + "/flat/64.png";
    },
  },
};
</script>

<template>
  <div class="row row-cols-4 g-4">
    <!--  <div class="col">
      <div class="img bg-danger">
        <img
          src="https://picsum.photos/id/58/306/480"
          alt=""
        />
      </div>
    </div>
    <div class="col">
      <div class="img bg-danger">
        <img
          src="https://picsum.photos/id/255/306/480"
          alt=""
        />
      </div>
    </div>
    <div class="col">
      <div class="img bg-danger">
        <img
          src="https://picsum.photos/id/978/306/480"
          alt=""
        />
      </div>
    </div>
    <div class="col">
      <div class="img bg-danger">
        <img
          src="https://picsum.photos/id/469/306/480"
          alt=""
        />
      </div>
    </div> -->

    <div
      class="col"
      v-for="movie in store.movieList"
    >
      <div class="info bg-success text-center">
        <h2>{{ movie.title }}</h2>
        <h3>{{ movie.original_title }}</h3>
        <!-- bandiera -->
        <div>{{ movie.original_language }}</div>
        <div>
          <img
            :src="getFlag(movie.original_language)"
            alt=""
          />
        </div>
        <!-- voto -->
        <div>{{ movie.vote_average }}</div>
        <div>
          <span>Trama</span>
          <p class="plot text-start">
            {{ movie.overview }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.col {
  height: 30rem;

  .img,
  .info {
    height: 100%;
    display: flex;
    flex-direction: column;
    padding: 1rem;
    gap: 1rem;

    .plot {
      min-height: 100%;
      overflow: auto;
    }
  }
}
</style>
