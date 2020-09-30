<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800;900&family=Pacifico&display=swap");
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}
html {
  box-sizing: border-box;
  font-size: 62.5%;
}
body {
  font-family: Montserrat, sans-serif;
  color: #312d2d;
}
#app {
  margin: 0;
  padding: 0;
}
</style>
