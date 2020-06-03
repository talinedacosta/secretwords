<template>
  <section id="game">
    <SecretWords />
  </section>
</template>

<script>
import SecretWords from "@/components/SecretWords.vue";

export default {
  name: "Game",
  components: {
    SecretWords
  }
};
</script>

<style lang="scss" scoped>
//
</style>
