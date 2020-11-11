<template>
  <q class="quote" :class="displayButton === false && 'add-quote'">
    {{ quote }}
  </q>
</template>

<script>
export default {
  props: ["quote", "displayButton"],
};
</script>

<style scoped>
.quote {
  align-self: flex-end;
  color: white;
  font-size: 45px;
  font-family: "Montserrat", sans-serif;
  font-style: italic;
  text-align: center;
  word-break: break-word;
  white-space: pre-wrap;
  line-height: 1.4;
}

.add-quote {
  align-self: center;
}
</style>