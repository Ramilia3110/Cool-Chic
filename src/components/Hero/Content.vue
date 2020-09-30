<template>
  <div class="content">
    <img class="hero1" src="@/assets/hero1.png" alt />
    <h1>
      Find your own
      <span>Chic</span>
    </h1>
    <img class="hero2" src="@/assets/hero2.png" alt />
  </div>
</template>

<script>
export default {
  name: "Content",
};
</script>

<style scoped lang="scss">
.content {
  position: relative;
  margin-top: 7rem;
  grid-column: 2 / span 10;
  grid-row: 2/3;
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  img {
    width: 30rem;
    height: 32rem;
  }
  .hero1 {
    align-self: flex-start;
  }
  .hero2 {
    align-self: flex-end;
  }
  h1 {
    font-family: Pacifico, sans-serif;
    font-weight: normal;
    font-size: 4.5rem;
    padding: 0 6rem;
    line-height: 10rem;
    text-align: center;

    color: #899cec;
    span {
      color: #fff;
    }
  }
}
@media screen {
  @media only screen and (max-width: 1150px) {
    .content {
      flex-direction: column;

      .hero1 {
        align-self: center;
        justify-self: center;
        max-width: 100%;
      }
      .hero2 {
        display: none;
      }
    }
  }
}

@media only screen and (max-width: 768px) {
  .content {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    .hero2 {
      display: none;
    }
    h1 {
      text-align: center;
      font-size: 3rem;
    }
  }
}
</style>
