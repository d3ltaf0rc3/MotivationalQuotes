<template>
  <div class="container">
    <Quote v-bind:displayButton="displayButton" v-bind:quote="this.displayedQuote" />
    <span v-if="displayButton" v-on:click="getNewQuote()" role="button"
      ><i class="fas fa-redo"></i>Get another one!</span
    >
  </div>
</template>

<script>
import Quote from "./Quote";
import quotes from "../assets/quotes.json";

export default {
  components: {
    Quote,
  },
  data() {
    return {
      displayedQuote: this.quote
    }
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
@import url(https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.1/css/all.min.css);
@import url("https://fonts.googleapis.com/css2?family=Montserrat&display=swap");

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

i {
  margin-right: 5px;
}

span {
  align-self: flex-end;
  color: #dadada;
  font-size: 18px;
  border-bottom: 2px solid #dadada;
  padding: 3px 2px;
  cursor: pointer;
  user-select: none;
}
</style>