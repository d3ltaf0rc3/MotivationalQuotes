<template>
  <div class="container">
    <QuoteBox class="quote-container" v-bind:quote="this.quote" v-bind:displayButton="true" />
  </div>
</template>

<script>
import QuoteBox from "../components/QuoteBox.vue";
import quotes from "../assets/quotes.json";

export default {
  components: {
    QuoteBox,
  },
  data() {
    return {
      quote: quotes[parseInt(Math.random() * (quotes.length - 0) + 0)],
    };
  },
};
</script>

<style scoped>
.container {
  display: grid;
  place-items: center;
  height: calc(100vh - 129px);
}

.quote-container {
  width: 60%;
  height: 65%;
}
</style>
