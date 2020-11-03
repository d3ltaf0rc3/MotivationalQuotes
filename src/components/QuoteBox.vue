<template>
  <div class="container">
    <Quote />
  </div>
</template>

<script>
import Quote from "./Quote.vue";

export default {
  name: "QuoteBox",
  components: {
    Quote,
  },
};
</script>

<style scoped>
.container {
  height: 60vh;
  width: 60vw;
  margin: 100px auto 0;
  background-color: rgba(155, 155, 155, 0.8);
  border-radius: 15px;
  box-shadow: 0px 0px 9px 0px rgba(0, 0, 0, 0.75);
  padding: 60px;
  display: grid;
  place-items: center;
}
</style>