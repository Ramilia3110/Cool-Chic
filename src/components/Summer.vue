<template>
  <div class="summer">
    <div class="container">
      <div class="inner-container">
        <div class="collections">
          <div class="content">
            <div class="main-model">
              <img src="@/assets/summer.png" alt />
            </div>
            <div class="summer-collection">
              <h2 class="header">Summer collection</h2>
              <p class="subHeader">
                All the new trends of the new coming season
              </p>

              <div class="accessories">
                <div
                  class="card"
                  v-for="card in accessoriesCards"
                  :key="card.id"
                >
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
          <div class="summer-models">
            <div
              class="sumCard"
              v-for="card in sumcollectionCards"
              :key="card.id"
            >
              <img class="sumModel" v-bind:src="card.modelImg" alt />
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
  name: "Summer",
  data() {
    return {
      accessoriesCards: [
        {
          id: 1,
          modelImg: require("@/assets/s1.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "320",
        },
        {
          id: 2,
          modelImg: require("@/assets/s2.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "280",
        },
        {
          id: 3,
          modelImg: require("@/assets/s3.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "230",
        },
      ],
      sumcollectionCards: [
        {
          id: 1,
          modelImg: require("@/assets/sum1.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "320",
        },
        {
          id: 2,
          modelImg: require("@/assets/sum2.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "280",
        },
        {
          id: 3,
          modelImg: require("@/assets/sum3.png"),
          name: "Black suit/dress",
          likeNumber: "1,305",
          feedbackNumber: "125",
          price: "230",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.summer {
  background: linear-gradient(
    0.05deg,
    rgba(255, 251, 150, 0.56) -0.87%,
    rgba(255, 251, 150, 0.4) 20.25%,
    rgba(255, 251, 150, 0.8) 38.4%,
    rgba(255, 251, 150, 0.4) 57.65%,
    rgba(255, 251, 150, 0.56) 80.54%,
    rgba(255, 251, 150, 0.56) 80.54%
  );
  overflow: hidden;
}

.collections {
  grid-column: 2 / span 10;
  margin: 20rem 0;
}
.content {
  height: 90vh;
  display: flex;
  justify-content: space-between;
}

.main-model {
  height: 50rem;
  img {
    max-height: 100%;
  }
}
.summer-collection {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  .header {
    font-size: 5rem;
  }
  .subHeader {
    font-size: 1.8rem;
    font-weight: 500;
    margin-top: 1.8rem;
  }
}

.accessories {
  margin-top: 5rem;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.card {
  text-align: center;
  height: 17rem;
  margin: 0 2.3rem;
  .model {
    max-height: 100%;
  }
  h4 {
    margin-top: 1rem;
    font-size: 1.6rem;
    font-weight: 700;
  }
  .text-content {
    margin: 2rem 0.5rem;
    display: flex;
    justify-content: space-between;
    .text-icon {
      height: 2.1rem;
      width: 2.7rem;
    }
    p {
      font-size: 1.4rem;
      font-weight: 600;
      span {
        color: #899cec;
      }
    }
  }
}
.card:last-child {
  margin-right: 0;
}
.card:first-child {
  margin-left: 0;
  padding-left: 0;
}

.summer-models {
  margin-top: 17rem;
  grid-column: 2 / span 10;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
  text-align: center;
  .sumCard {
    height: 35rem;
    .sumModel {
      max-height: 100%;
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
}
@media only screen and (max-width: 1200px) {
  .content {
    // flex-direction: column;
    height: auto;
    // align-items: center;
    .main-model {
      height: 40rem;
    }
    .summer-collection {
      align-items: center;
      .accessories {
        .card {
          height: 13rem;
          margin: 0;
        }
      }
    }
  }

  .card h4 {
    font-size: 1.4rem;
  }
  .card .text-content {
    margin: 1rem 0.5rem;
    .text-icon {
      height: 1.8rem;
      width: 2.4rem;
    }
    p {
      font-size: 1.2rem;
      font-weight: 600;
      padding-right: 0.5rem;
    }
  }
}
@media only screen and (max-width: 1000px) {
  .content .main-model {
    height: 30rem;
  }
}
@media only screen and (max-width: 900px) {
  .collections {
    margin-bottom: 3.5rem;
  }
  .summer {
    position: relative;
  }
  .content .main-model {
    height: 40rem;
  }
  .content {
    flex-direction: column;
    align-items: center;
    justify-content: center;
    .summer-collection .accessories {
      justify-content: center;
      flex-wrap: initial;
      padding: 0;
      margin: 0;
      .card {
        margin-top: 3rem;
      }
    }
  }

  .summer-collection {
    .header {
      position: absolute;
      top: 4.5%;
      font-size: 3rem;

      font-weight: 700;
    }
    .subHeader {
      position: absolute;
      top: 5.5%;
      font-size: 1.5rem;
    }
  }

  .card {
    h4 {
      margin-top: 0.8rem;
      font-size: 1.3rem;
      font-weight: 500;
    }
    .text-content {
      margin: 0.5rem;
      display: flex;

      .text-icon {
        height: 1.3rem;
        width: 1.9rem;
      }
      p {
        font-size: 1rem;
        font-weight: 400;

        span {
          color: #899cec;
        }
      }
    }
  }
  .summer-models {
    .sumCard {
      height: 40rem;
      padding: 0 0 11rem 0;
      h4 {
        font-weight: 600;
        font-size: 1.6rem;
      }
      .text-content {
        margin: 1rem;
        .text-icon {
          height: 1.7rem;
          width: 2.3rem;
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
  }
}
</style>
