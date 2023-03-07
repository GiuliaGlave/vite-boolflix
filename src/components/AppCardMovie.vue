<script>
export default {
  data() {
    return {};
  },
};
</script>

<template>
  <div class="row row-cols-4 g-4">
    <div class="col">
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
    </div>

    <div class="col">
      <div class="info bg-success text-center">
        <div>
          <h2>titolo</h2>
          <h3>titolo originale</h3>
          <div>lingua</div>
          <div>voto</div>
          <div>
            <span>Trama</span>
            <p>
              testo trama Lorem ipsum dolor sit amet consectetur adipisicing
              elit. Tempora, libero.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="col">
      <div class="info bg-success text-center">
        <div>
          <h2>titolo</h2>
          <h3>titolo originale</h3>
          <div>lingua</div>
          <div>voto</div>
          <div>
            <span>Trama</span>
            <p>
              testo trama Lorem ipsum dolor sit amet consectetur adipisicing
              elit. Tempora, libero.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="col">
      <div class="info bg-success text-center">
        <div>
          <h2>titolo</h2>
          <h3>titolo originale</h3>
          <div>lingua</div>
          <div>voto</div>
          <div>
            <span>Trama</span>
            <p>
              testo trama Lorem ipsum dolor sit amet consectetur adipisicing
              elit. Tempora, libero.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="col">
      <div class="info bg-success text-center">
        <div>
          <h2>titolo</h2>
          <h3>titolo originale</h3>
          <div>lingua</div>
          <div>voto</div>
          <div>
            <span>Trama</span>
            <p>
              testo trama Lorem ipsum dolor sit amet consectetur adipisicing
              elit. Tempora, libero.
            </p>
          </div>
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
    div {
      display: flex;
      flex-direction: column;
      padding: 1rem;
    }
  }
}
</style>
