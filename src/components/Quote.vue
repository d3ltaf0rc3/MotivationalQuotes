<template>
  <p class="quote">
    "{{ quote }}"
  </p>
</template>

<script>
import quotes from "../assets/quotes.json";

export default {
  name: "Quote",
  data() {
    return {
      quote: quotes[parseInt(Math.random() * (quotes.length - 0) + 0)],
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Montserrat&display=swap");
.quote {
  color: white;
  font-size: 48px;
  font-family: "Montserrat", sans-serif;
  font-style: italic;
  text-align: center;
  word-break: break-word;
  white-space: pre-wrap;
}
</style>