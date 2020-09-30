<template>
  <div class="contact">
    <div class="container">
      <div class="inner-container">
        <div class="partners">
          <img class="p1" src="@/assets/p1.svg" alt />
          <img class="p2" src="@/assets/p2.svg" alt />
          <img class="p3" src="@/assets/p3.svg" alt />
          <img class="p4" src="@/assets/p4.svg" alt />
          <img class="p5" src="@/assets/p5.svg" alt />
        </div>

        <div class="contact-form">
          <div class="contact-img">
            <img src="@/assets/contact.png" alt />
          </div>

          <div class="form">
            <h1>Contact us</h1>
            <form id="f1">
              <table style="width:100%">
                <tr>
                  <th>
                    <input
                      type="text"
                      name="firstname"
                      placeholder="First Name"
                      v-model="user.name"
                      required
                      class="fname"
                    />
                  </th>
                  <th>
                    <input
                      type="text"
                      name="lastname"
                      placeholder="Last Name"
                      v-model="user.name"
                      required
                      class="lname"
                    />
                  </th>
                </tr>
                <tr>
                  <th>
                    <input
                      type="text"
                      name="phone"
                      id="phone"
                      placeholder="Phone"
                      required
                      class="phone"
                    />
                  </th>
                  <th>
                    <input
                      type="email"
                      name="email"
                      placeholder="Email"
                      required="required"
                      v-model="user.email"
                      class="email"
                    />
                  </th>
                </tr>
                <tr>
                  <th colspan="4">
                    <textarea
                      placeholder="Type your message here ..."
                      cols="20"
                      class="message"
                    ></textarea>
                  </th>
                </tr>
              </table>

              <input type="submit" class="btn" value="Submit" />
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact",
  data() {
    return {
      user: {
        name: "",
        email: "",
      },
    };
  },
};
</script>

<style scoped lang="scss">
$primaryBG: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.5) 0%,
    rgba(255, 255, 255, 0) 100%
  ),
  linear-gradient(
    226.97deg,
    rgba(141, 253, 211, 0.6) 20.73%,
    rgba(107, 108, 230, 0.6) 41.91%,
    rgba(255, 251, 150, 0.6) 60.03%,
    rgba(1, 205, 254, 0.6) 79.44%,
    rgba(163, 221, 199, 0.6) 89.91%
  );
.contact {
  overflow: hidden;
  margin-top: 15rem;
  height: 150vh;
  background: #fff;
}
.partners {
  margin-top: 5rem;
  grid-column: 2 / span 10;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .p1 {
    max-height: 13rem;
    max-width: 11rem;
  }
  .p2 {
    max-height: 22rem;
    max-width: 20rem;
  }
  .p3 {
    max-height: 16rem;
    max-width: 14rem;
  }
  .p4 {
    max-height: 20rem;
    max-width: 18rem;
  }
  .p5 {
    max-height: 14rem;
    max-width: 12rem;
  }
}
.contact-form {
  margin-top: 30rem;
  grid-column: 2 / span 10;
  display: flex;
  justify-content: space-between;

  .contact-img {
    flex: 1;
    height: 40rem;
    img {
      max-width: 100%;
      max-height: 100%;
    }
  }

  .form {
    flex: 1;
    text-align: center;
    align-self: flex-end;
    h1 {
      font-size: 5rem;
      font-weight: 800;
      margin-bottom: 5rem;
    }
  }
}

table {
  border-collapse: collapse;
}

th {
  border: 2px solid #312d2d;
  margin: 0;
  &:hover {
    border-color: #02889c;
  }
  input {
    height: 7vh;
  }
  textarea {
    height: 15vh;
  }
  input,
  textarea {
    padding: 2.5rem;
    font-size: 1.6rem;
    border: none;
    width: 100%;
    &:focus {
      outline: none;
    }
  }
}

.btn {
  border: none;
  width: 100%;
  border-radius: 1rem;
  padding: 1rem 3rem;
  margin: 3rem 0 1rem 0;
  background: linear-gradient(
    0.05deg,
    rgba(255, 251, 150, 0.56) -0.87%,
    rgba(255, 251, 150, 0.4) 20.25%,
    rgba(255, 251, 150, 0.8) 38.4%,
    rgba(255, 251, 150, 0.4) 57.65%,
    rgba(255, 251, 150, 0.56) 80.54%,
    rgba(255, 251, 150, 0.56) 80.54%
  );
  font-size: 1.8rem;
  font-weight: 500;
  cursor: pointer;
  &:hover {
    background: $primaryBG;
  }
}

.fname::-webkit-input-placeholder,
.lname::-webkit-input-placeholder,
.phone::-webkit-input-placeholder,
.email::-webkit-input-placeholder,
.message::-webkit-input-placeholder {
  color: #312d2d;
}
.message::-webkit-input-placeholder {
  font-size: 1.8rem;
}

.message {
  resize: none;
}

@media only screen and (max-width: 992px) {
  .contact {
    height: auto;
    overflow: auto;
    margin-top: 5rem;
  }
  .partners {
    justify-content: space-evenly;

    img {
      margin-right: 1rem;
    }
    .p1 {
      max-height: 10rem;
      max-width: 8rem;
    }
    .p2 {
      max-height: 14rem;
      max-width: 12rem;
    }
    .p3 {
      max-height: 12rem;
      max-width: 10rem;
    }
    .p4 {
      max-height: 13rem;
      max-width: 11rem;
    }
    .p5 {
      max-height: 11rem;
      max-width: 9rem;
    }
  }

  .contact-form {
    flex-direction: column;
    align-items: center;
    margin: 9rem 0;

    .contact-img {
      display: none;
    }
    .form {
      width: 100%;
      text-align: center;
      align-self: center;
      h1 {
        font-size: 3rem;
        font-weight: 800;
        margin-bottom: 1rem;
      }
    }
  }

  h1 {
    padding: 1rem 0 3rem 0;
    font-size: 5rem;
    font-weight: 400;
    text-align: center;
  }
}
@media only screen and (max-width: 768px) {
  .partners {
    max-width: 100%;
    margin: 0;
    img {
      margin-right: 1rem;
    }
    .p1 {
      max-height: 8rem;
      max-width: 6rem;
    }
    .p2 {
      max-height: 12rem;
      max-width: 10rem;
    }
    .p3 {
      max-height: 10rem;
      max-width: 8rem;
    }
    .p4 {
      max-height: 11rem;
      max-width: 9rem;
    }
    .p5 {
      max-height: 9rem;
      max-width: 7rem;
    }
  }
}
</style>
