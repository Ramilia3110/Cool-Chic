<template>
  <div class="hoodies">
    <div class="container">
      <h1>Cosmo Hoodies</h1>
      <div class="banner">
        <div class="inner-container">
          <div class="hoodies-content">
            <div class="card" v-for="card in hoodiesCards" :key="card.id">
              <img class="model" v-bind:src="card.modelImg" alt />
              <h4>{{ card.name }}</h4>
              <div class="text-content">
                <img class="text-icon" src="@/assets/like.svg" alt />
                <p>{{ card.likeNumber }}</p>
                <img class="text-icon" src="@/assets/feedback.svg" alt />
                <p>{{ card.feedbackNumber }}</p>
                <p>
                  <span>$</span>
                  {{ card.price }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hoodies",
  data() {
    return {
      hoodiesCards: [
        {
          id: 1,
          modelImg: require("@/assets/h1.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "320",
        },
        {
          id: 2,
          modelImg: require("@/assets/h2.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "280",
        },
        {
          id: 3,
          modelImg: require("@/assets/h3.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "129",
          price: "230",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
$primaryBg: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.5) 0%,
    rgba(255, 255, 255, 0) 100%
  ),
  linear-gradient(
    226.97deg,
    rgba(218, 159, 210, 0.6) 20.73%,
    rgba(170, 202, 221, 0.6) 41.91%,
    rgba(255, 251, 150, 0.6) 60.03%,
    rgba(230, 107, 189, 0.6) 79.44%,
    rgba(163, 221, 199, 0.6) 89.91%
  );
.hoodies {
  height: 100vh;
  overflow: hidden;
  background: $primaryBg;
  h1 {
    text-align: center;
    padding-top: 1rem;
    font-family: Pacifico, sans-serif;
    font-size: 4.5rem;
  }
  .banner {
    height: 70%;
  }
}
.hoodies-content {
  grid-column: 2 / span 10;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}
.card {
  text-align: center;
  height: 35rem;
  margin-top: 5rem;
  width: 30%;
  .model {
    max-height: 100%;
    max-width: 100%;
    object-fit: cover;
  }
  h4 {
    margin-top: 1rem;
    font-size: 1.8rem;
    font-weight: 700;
  }
  .text-content {
    margin: 2rem 0.5rem;
    display: flex;
    justify-content: center;
    .text-icon {
      height: 2.5rem;
      width: 3.1rem;
    }
    p {
      font-size: 1.6rem;
      font-weight: 600;
      margin-right: 1.5rem;
      span {
        color: #899cec;
      }
    }
  }
}

@media only screen and (max-width: 992px) {
  .hoodies {
    height: auto;
    h1 {
      font-size: 3.2rem;
      padding-top: 0.5rem;
    }
  }

  .hoddies .banner {
    height: min-content;
  }

  .hoodies-content {
    padding-bottom: 3rem;
    .card {
      height: 26rem;
      padding-bottom: 3rem;

      .model {
        margin-top: 0;
      }
      h4 {
        font-size: 1.4rem;
        font-weight: 700;
      }
      .text-content {
        margin: 0.5rem;
        justify-content: space-evenly;
        .text-icon {
          height: 1.2rem;
          width: 1.8rem;
        }
        p {
          font-size: 1rem;
          font-weight: 600;
          margin-right: 0;
        }
      }
    }
  }
}
</style>
