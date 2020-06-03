<template>
  <section>
    <p>Secret Words</p>
    <Keyboard :alphabet="alphabet" />
  </section>
</template>

<script>
import Keyboard from "./Keyboard.vue";

export default {
  name: "SecretWords",
  components: {
    Keyboard
  },
  data() {
    return {
      alphabet: "ABCDEFGHIJKLMNOPQRSTUVWYXZÇ"
    };
  }
};
</script>

<style lang="scss" scoped>
//
</style>
