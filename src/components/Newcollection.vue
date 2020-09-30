<template>
  <div class="newcollection">
    <h1>New collection</h1>
    <div class="container">
      <div class="inner-container">
        <div class="women-collection">
          <h3>Women</h3>
          <div class="content">
            <div class="card" v-for="card in womenCards" :key="card.id">
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

        <div class="men-collection">
          <h3>Men</h3>
          <div class="content">
            <div class="card" v-for="card in menCards" :key="card.id">
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
  name: "Newcollection",
  data() {
    return {
      womenCards: [
        {
          id: 1,
          modelImg: require("@/assets/1.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "320",
        },
        {
          id: 2,
          modelImg: require("@/assets/2.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "280",
        },
        {
          id: 3,
          modelImg: require("@/assets/3.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "230",
        },
        {
          id: 4,
          modelImg: require("@/assets/4.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "120",
        },
      ],
      menCards: [
        {
          id: 1,
          modelImg: require("@/assets/1.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "320",
        },
        {
          id: 2,
          modelImg: require("@/assets/2.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "280",
        },
        {
          id: 3,
          modelImg: require("@/assets/3.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "230",
        },
        {
          id: 4,
          modelImg: require("@/assets/4.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "120",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.newcollection {
  height: 200vh;
  background: linear-gradient(
    0.05deg,
    rgba(255, 251, 150, 0.56) -0.87%,
    rgba(255, 251, 150, 0.4) 20.25%,
    rgba(255, 251, 150, 0.8) 38.4%,
    rgba(255, 251, 150, 0.4) 57.65%,
    rgba(255, 251, 150, 0.56) 80.54%,
    rgba(255, 251, 150, 0.56) 80.54%
  );
  text-align: center;
  h1 {
    padding-top: 7rem;
    font-family: Pacifico, sans-serif;
    font-size: 4.5rem;
    line-height: 112px;
  }
}

.women-collection,
.men-collection {
  grid-column: 2 / span 10;
}
h3 {
  text-align: left;
  font-weight: 500;
  font-size: 3rem;
  padding-top: 7rem;
}
.content {
  margin-top: 3rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.card {
  text-align: center;
  height: 30rem;
  .model {
    max-height: 100%;
  }
  h4 {
    margin-top: 1rem;
    font-size: 1.8rem;
    font-weight: 700;
  }
  .text-content {
    margin: 1.2rem 0.5rem 4.1rem 0.5rem;
    display: flex;
    justify-content: space-between;
    .text-icon {
      height: 2.5rem;
      width: 3.1rem;
    }
    p {
      font-size: 1.6rem;
      font-weight: 600;
      span {
        color: #899cec;
      }
    }
  }
}
.men-collection {
  margin-top: 15rem;
}

@media only screen and (max-width: 1200px) {
  .newcollection {
    height: auto;
    overflow: auto;
  }
  .men-collection,
  .women-collection {
    margin-top: 5rem;
  }
  .card {
    margin-bottom: 9rem;
  }
}
@media only screen and (max-width: 768px) {
  .newcollection {
    h1 {
      padding-top: 1rem;
      font-size: 3rem;
    }
  }
  .men-collection,
  .women-collection {
    margin-top: 0;
  }

  .content {
    margin-top: 2rem;
  }
  .card {
    height: 25rem;
    h4 {
      margin-top: 0;
      font-size: 1.6rem;
      font-weight: 600;
    }
    .text-content {
      margin: 1.2rem 1rem;
      display: flex;
      justify-content: space-evenly;
      .text-icon {
        height: 1.8rem;
        width: 2.4rem;
      }
      p {
        font-size: 1.2rem;
        font-weight: 500;
        span {
          color: #899cec;
        }
      }
    }
  }

  h3 {
    text-align: center;
    font-size: 2.1rem;
    font-weight: 800;
    padding-top: 3rem;
  }
}
</style>
