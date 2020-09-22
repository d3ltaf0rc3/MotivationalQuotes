<template>
  <div id="app">
    <QuoteBox />
  </div>
</template>

<script>
import QuoteBox from './components/QuoteBox.vue';

export default {
  name: "App",
  components: {
    QuoteBox
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}

#app {
  background-image: url("./assets/background.jpg");
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: center;
  height: 100vh;
  display: grid;
  align-items: center;
  justify-content: center;
}
</style>
