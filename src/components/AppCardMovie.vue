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
    <div
      class="col"
      v-for="movie in store.movieList"
    >
      <!-- poster -->
      <div class="img">
        <img
          :src="`https://image.tmdb.org/t/p/w200${movie.poster_path}`"
          alt="poster"
        />
      </div>
      <div class="info text-center">
        <h2>{{ movie.title }}</h2>
        <h3>{{ movie.original_title }}</h3>
        <!-- bandiera -->

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
  position: relative;
  transition: transform 1000ms;
  transform-style: preserve-3d;

  &:hover {
    cursor: pointer;
    transform: rotateY(180deg);
  }

  .img,
  .info {
    max-width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;

    gap: 1rem;
    position: absolute;
    backface-visibility: hidden;
  }
  .info {
    background-color: black;
    transform: rotateY(180deg);
    padding: 1rem;
  }
  .plot {
    min-height: 100%;
    overflow: auto;
  }
  img {
    height: 100%;
  }
}
</style>
