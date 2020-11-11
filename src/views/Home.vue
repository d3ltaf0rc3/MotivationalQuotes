<template>
  <QuoteBox v-bind:quote="this.quote" v-bind:displayButton="true" />
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