<script>
export default {
  data() {
    return {
      wordSearched: "",
    };
  },
  props: {
    name: String,
    placeholder: String,
    search: String,
  },
  emits: ["newSearch"],
};
</script>

<template>
  <header class="bg-dark">
    <div class="container">
      <nav class="navbar w-100">
        <div class="container-fluid">
          <a class="navbar-brand fs-1 text-danger">{{ name }}</a>
          <form
            class="d-flex"
            role="search"
            @submit.prevent="$emit('newSearch', wordSearched)"
          >
            <input
              class="form-control me-2"
              type="search"
              :placeholder="placeholder"
              aria-label="Search"
              v-model="wordSearched"
            />
            <button
              class="btn btn-outline-danger"
              type="submit"
            >
              {{ search }}
            </button>
          </form>
        </div>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap");

* {
  font-family: "Bebas Neue", cursive;
}
header {
  height: 5rem;
  .container {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>
