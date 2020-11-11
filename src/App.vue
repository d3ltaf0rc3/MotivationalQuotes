<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/all">See all quotes</router-link>
    </div>
    <router-view />
    <img class="background" src="./assets/background.jpg" alt="background" />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: "Roboto", sans-serif;
}

.background {
  height: 100vh;
  width: 100%;
  position: fixed;
  z-index: -1;
  top: 0;
}

#nav {
  padding: 50px 0 30px;
  text-align: center;
}

#nav a {
  color: #ffffff;
  text-decoration: none;
  font-size: 24px;
  margin: 0 15px;
}

#nav a.router-link-exact-active {
  color: #00624d;
  border-bottom: 3px solid #00624d;
}
</style>
