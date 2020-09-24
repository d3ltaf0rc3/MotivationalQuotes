<template>
    <div class="container">
        <Quote />
    </div>
</template>

<script>
import Quote from './Quote.vue';

export default {
    name: "QuoteBox",
    components: {
        Quote
    }
}
</script>

<style scoped>
    .container {
        height: 60vh;
        width: 60vw;
        background-color: rgba(155, 155, 155, 0.8);
        border-radius: 15px;
        box-shadow: 1px 1px #000;
        padding: 50px;
        display: grid;
        place-items: center;
    }
</style>