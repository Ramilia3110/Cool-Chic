<template>
  <div class="hero">
    <div class="container">
      <div class="inner-box">
        <Header />
        <Content />
        <div class="ppp">
          <button>Shop now!!!</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./Hero/Header";
import Content from "./Hero/Content";
export default {
  name: "Hero",
  components: {
    Header,
    Content,
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hero {
  height: 100vh;
  padding: 0;
  margin: 0;
  overflow: hidden;
  background: #37284d;
  // background: linear-gradient(
  //   0.05deg,
  //   rgba(255, 251, 150, 0.56) -0.87%,
  //   rgba(255, 251, 150, 0.4) 20.25%,
  //   rgba(255, 251, 150, 0.8) 38.4%,
  //   rgba(255, 251, 150, 0.4) 57.65%,
  //   rgba(255, 251, 150, 0.56) 80.54%,
  //   rgba(255, 251, 150, 0.56) 80.54%
  // );

  .inner-box {
    // background: #312d2d;
    width: 100%;
    height: 75vh;
    display: grid;
    margin-top: 0;
    grid-template-columns: repeat(12, 1fr);
    grid-auto-rows: 15vh 60vh 15vh min-content;
    grid-column-gap: 20px;
  }
}
.ppp {
  grid-row: 3/4;
  height: 10vh;
  text-align: center;
  grid-column: 2 / span 10;

  button {
    font-weight: 600;
    font-size: 1.6rem;
    background: rgba(255, 255, 255, 0.15);
    border: 3px solid #fffdc7;
    border-radius: 1.5rem;
    color: #fffdd0;
    padding: 0.5rem 3rem;
    margin-top: 10rem;
    &:hover {
      background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 0.5) 0%,
          rgba(255, 255, 255, 0) 100%
        ),
        linear-gradient(
          226.97deg,
          rgba(141, 253, 211, 0.42) 18.98%,
          rgba(137, 156, 236, 0.6) 31.28%,
          rgba(107, 108, 230, 0.6) 39.34%,
          rgba(255, 251, 150, 0.6) 60.03%,
          rgba(1, 205, 254, 0.6) 73.01%,
          rgba(255, 113, 206, 0.6) 88.91%
        );
    }
  }
}
</style>
