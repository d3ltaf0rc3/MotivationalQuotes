<template>
  <div class="grid-container">
    <QuoteBox
      class="grid-item"
      v-bind:displayButton="false"
      v-bind:quote="quote"
      v-for="quote in quotes"
      :key="quote"
    />
  </div>
</template>

<script>
import QuoteBox from "../components/QuoteBox";
import quotes from "../assets/quotes.json";

export default {
  components: {
    QuoteBox,
  },
  data() {
    return {
      quotes,
    };
  },
};
</script>

<style scoped>
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  padding-bottom: 50px;
}

.grid-item {
  width: 800px;
}
</style>