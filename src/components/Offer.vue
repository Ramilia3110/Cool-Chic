<template>
  <div class="offer">
    <div class="container">
      <div class="banner">
        <div class="inner-container">
          <div class="content">
            <div class="img-content">
              <img src="@/assets/perfume.svg" alt />
            </div>

            <div class="text-content">
              <h4>Special offer</h4>
              <h1>70% discount</h1>
              <p>
                Lorem ipsum dolor sit, amet consectetur
                adipisicing elit. Eius eum illo quaerat sunt placeat
                repellat atque ex.
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Offer",
};
</script>

<style  scoped lang="scss">
.offer {
  margin: 0;
  padding: 0;
  height: 100vh;
  overflow: hidden;
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

.banner {
  max-width: 100%;
  height: 80vh;
  margin-top: 10vh;
  background: linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.9) 0%,
      rgba(255, 255, 255, 0) 100%
    ),
    linear-gradient(
      226.97deg,
      rgba(141, 253, 211, 0.63) 18.98%,
      rgba(137, 156, 236, 0.9) 31.28%,
      rgba(107, 108, 230, 0.9) 39.34%,
      rgba(255, 251, 150, 0.9) 60.03%,
      rgba(1, 205, 254, 0.9) 73.01%,
      rgba(255, 113, 206, 0.9) 88.91%
    );
  box-shadow: 0px 4px 4px rgba(255, 253, 208, 0.2);
  .content {
    grid-column: 2 / span 10;
    max-width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .img-content {
      flex: 1;
      order: 1;
      img {
        padding-top: 3rem;
        height: 50rem;
      }
    }
    .text-content {
      order: 2;
      text-align: center;
      flex: 1;
      max-width: 100%;
      h4 {
        font-weight: 900;
        font-size: 3rem;
        color: #ff71ce;
        margin-bottom: 0.5rem;
      }
      h1 {
        color: #fff;
        font-size: 8rem;
        font-weight: 900;
        margin-bottom: 1.5rem;
      }
      p {
        font-size: 1.8rem;
      }
    }
  }
}
@media only screen and (max-width: 1200px) {
  .offer {
    height: auto;
  }
  .banner .content {
    .img-content img {
      height: 40rem;
    }
    .text-content {
      h4 {
        font-size: 2rem;
      }
      h1 {
        font-size: 5rem;
        font-weight: 900;
      }
    }
  }
}
@media only screen and (max-width: 768px) {
  .banner .content {
    flex-direction: column;
    .img-content {
      order: 2;
      img {
        height: 35rem;
      }
    }
    .text-content {
      order: 1;
      padding-top: 5rem;
      p {
        font-size: 1.4rem;
      }
    }
  }
}
</style>