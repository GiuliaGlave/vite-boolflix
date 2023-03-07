<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <header class="bg-dark">
    <div class="container">
      <nav class="navbar w-100">
        <div class="container-fluid">
          <a class="navbar-brand fs-1 text-light">BOOLFLIX</a>
          <form
            class="d-flex"
            role="search"
          >
            <input
              class="form-control me-2"
              type="search"
              placeholder="Search"
              aria-label="Search"
            />
            <button
              class="btn btn-outline-danger"
              type="submit"
            >
              Search
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
