<template>
  <nav class="nav">
    <router-link to="/">Home</router-link>
    <router-link to="/all">See all quotes</router-link>
  </nav>
</template>

<style scoped>
.nav {
  padding: 50px 0;
  text-align: center;
}

.nav a {
  color: #ffffff;
  text-decoration: none;
  font-size: 24px;
  margin: 0 15px;
}

.nav a.router-link-exact-active {
  color: #00624d;
  border-bottom: 3px solid #00624d;
}
</style>
