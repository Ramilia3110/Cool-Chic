<template>
  <div class="footer">
    <div class="container">
      <div class="inner-container">
        <div class="footer-items">
          <div class="box">
            <div class="logo">
              Cool
              <span class="chic">Chic</span>
            </div>
            <img class="app" src="@/assets/google play.svg" alt />
            <img class="app" src="@/assets/app store.svg" alt />
          </div>
          <div class="box">
            <h4>Useful Links</h4>
            <ul class="social-links">
              <li>
                <a href>Instagram</a>
              </li>
              <li>
                <a href>LinkedIn</a>
              </li>
              <li>
                <a href>Facebook</a>
              </li>
              <li>
                <a href>Twitter</a>
              </li>
            </ul>
          </div>
          <div class="box">
            <h4>Addresss</h4>
            <div class="address">
              <p>19, Zako Street,</p>
              <p>720040 Bishkek,</p>
              <p>Kyrgyz Republic</p>
              <p>Tel.: +996 312 39-81-62,</p>
              <p>00 996 312 39-81-63</p>
            </div>
          </div>
        </div>
        <div class="copyright">
          <p><span>&#169;</span> 2020 All rights reserved</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss">
.footer {
  background: #312d2d;
  height: 40rem;
  .footer-items {
    padding: 5rem 0;
    grid-column: 2 / span 10;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
  }
}
.box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  color: #fff;
  font-size: 1.6rem;
  font-weight: normal;
  h4 {
    padding: 2rem 0;
    font-size: 1.8rem;
  }
}
.social-links {
  list-style: none;
  li a {
    color: #fff;
    text-decoration: none;
    margin: 2rem 0;
  }
}

p,
li {
  margin-bottom: 1.5rem;
}
.logo {
  font-family: Pacifico;
  font-style: normal;
  font-weight: normal;
  font-size: 3.8rem;
  color: #ff71ce;

  .chic {
    color: #899cec;
  }
}
.app {
  height: 6rem;
  width: 22rem;
  margin: 1rem 0;
}
.copyright {
  margin-top: 3rem;
  color: #fff;
  grid-column: 2 / span 10;
  font-size: 1.4rem;
  text-align: center;
  span {
    font-size: 1.7rem;
    padding-top: 1rem;
  }
}
@media only screen and (max-width: 768px) {
  .footer {
    height: auto;
  }
  .box {
    font-size: 1.2rem;
    font-weight: 400;
    margin: 2rem 3rem 1.5rem 0;

    h4 {
      padding: 1rem 0;
      font-size: 1.4rem;
      font-weight: 500;
    }
  }
  .social-links li a {
    margin: 1rem 0;
  }

  p,
  li {
    margin-bottom: 1rem;
  }
  .logo {
    font-size: 3rem;
  }
  .app {
    height: 3rem;
    width: 12rem;
    margin: 1rem 0;
  }
  .copyright {
    margin-top: 1rem;
    color: #fff;
    grid-column: 2 / span 10;
    font-size: 1.2rem;
    text-align: center;
    span {
      font-size: 1.7rem;
      padding-top: 1rem;
    }
  }
}
</style>
