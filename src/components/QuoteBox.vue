<template>
  <div class="container">
    <q class="quote">
      {{ this.displayedQuote }}
    </q>
    <span class="btn" v-if="displayButton" v-on:click="getNewQuote()" role="button">
      <i class="fas fa-redo"></i>Get another one!
    </span>
  </div>
</template>

<script>
import quotes from "../assets/quotes.json";

export default {
  data() {
    return {
      displayedQuote: this.quote,
    };
  },
  methods: {
    getNewQuote() {
      this.displayedQuote = quotes[parseInt(Math.random() * (quotes.length - 0) + 0)];
    },
  },
  props: ["displayButton", "quote"],
};
</script>

<style scoped>
.container {
  background-color: rgba(155, 155, 155, 0.8);
  border-radius: 15px;
  box-shadow: 0px 0px 9px 0px rgba(0, 0, 0, 0.75);
  padding: 60px;
  text-align: center;
}

.quote {
  color: #fff;
  font-size: 45px;
  font-family: "Montserrat", sans-serif;
  font-style: italic;
  word-break: break-word;
  white-space: pre-wrap;
  line-height: 1.4;
}

.btn {
  display: inline-block;
  color: #dadada;
  font-size: 18px;
  border-bottom: 2px solid #dadada;
  padding: 3px 2px;
  cursor: pointer;
  user-select: none;
  align-self: flex-end;
}

.btn i {
  margin-right: 5px;
}
</style>
