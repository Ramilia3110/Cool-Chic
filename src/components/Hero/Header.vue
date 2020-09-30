<template>
  <div class="header">
    <nav>
      <input type="checkbox" id="menu" />
      <label for="menu" class="menu-btn">
        <img src="@/assets/menu.svg" />
      </label>
      <div class="logo">
        <span class="menu"></span>
        Cool
        <span class="chic">Chic</span>
      </div>

      <div class="nav-links">
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">Men</a>
        </li>
        <li>
          <a href="#">Women</a>
        </li>
        <li>
          <a href="#">Promotions</a>
        </li>
        <li>
          <a href="#">Contact Us</a>
        </li>
      </div>
    </nav>

    <div class="right-blog">
      <a href="#">
        <img class="profile" src="@/assets/profile.svg" alt />
      </a>
      <a href="#">
        <img class="cart" src="@/assets/cart.svg" alt />
      </a>
      <div class="s-box">
        <input type="checkbox" id="search" />
        <label for="search" class="search-icon">
          <img src="@/assets/search.svg" />
        </label>

        <div class="search-box">
          <form action>
            <input type="text" class="searchField" />
            <input type="submit" value="Go" class="sub" />
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
.header {
  position: relative;
  height: 8vh;
  margin-top: 25px;
  grid-column: 2 / span 10;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
nav {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}
#menu,
.menu-btn {
  display: none;
}
.logo {
  font-family: Pacifico;
  margin-right: 3rem;
  font-weight: normal;
  font-size: 3rem;
  color: #ff71ce;

  .chic {
    color: #899cec;
  }
}

.nav-links {
  display: flex;
  list-style: none;
  font-family: Montserrat;
  font-weight: 500;
  font-size: 1.8rem;
  a {
    margin-right: 15px;
    text-decoration: none;
    color: #fff;
  }
}

.right-blog {
  display: flex;
  align-items: center;
  justify-content: space-between;
  img {
    margin-left: 1.8rem;
    height: 2.5rem;
    width: 2.5rem;
  }
  img:last-child {
    margin-right: 0;
  }
}

#search {
  display: none;
}

.search-box {
  position: absolute;
  right: 3.5%;
  top: -10rem;
  width: 30rem;
  height: 4.5rem;
  padding: 1rem;
  background-color: #1e232b;
  border-radius: 0.4rem;
  box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.5);
  transition: all 0.17s ease;
}

form {
  width: 100%;
  height: 3rem;
  right: 0;
  background-color: #9b9b9b08;
  display: flex;
  overflow: hidden;
  padding: 2px;
  border: 1px solid #9b9b9b33;
  border-radius: 0.4rem;
}

.searchField {
  width: 95%;
  background-color: #111111;
  color: #ff71ce;
  padding: 0 1rem;
  font-family: inherit;
  font-size: 1.4rem;
  font-weight: 400;
  border: 0;
  outline: none;
}

.sub {
  font-size: 1.4rem;
  padding: 0 1.3rem;
  border: 0;
  background: #fffb96;
  border-radius: 4px;
  cursor: pointer;
}
.sub:hover {
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
#search:checked ~ .search-box {
  top: 5rem;
}

@media only screen and (max-width: 1052px) {
  .header {
    position: relative;
    height: auto;
  }
  nav {
    width: 100%;
    justify-content: left;
    align-items: center;
  }
  .nav-links {
    position: fixed;
    top: -80rem;
    left: 11.7%;
    width: 30rem;
    height: 100vh;
    padding-top: 10rem;
    z-index: 2;
    background-color: #12161d;
    flex-direction: column;
    transition: all 0.5s;
  }
  .nav-links li {
    padding: 1rem 5rem;
  }

  .menu-btn {
    display: block;
    left: 0;
    top: 0;
    z-index: 3;
    img {
      width: 5rem;
      height: 5rem;
    }
  }
  .logo {
    padding-bottom: 1rem;
  }
  #menu:checked ~ .nav-links {
    top: 13%;
  }
}

@media only screen and (max-width: 768px) {
  .nav-links {
    width: 50%;
  }
}
</style>
