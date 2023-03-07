<script>
import { store } from "../data/store";
export default {
  data() {
    return {
      store,
    };
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
        <div>{{ movie.original_language }}</div>
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
