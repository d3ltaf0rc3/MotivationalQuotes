<template>
  <div class="grid-container">
    <QuoteBox
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
  padding: 50px 100px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
}
</style>