<template>
  <div class="keyboard">
    <key v-for="(key, index) in alphabetToLowerCase" :key="index">{{
      key
    }}</key>
  </div>
</template>

<script>
import { bus } from "@/main.js";

import Key from "./Key.vue";

export default {
  name: "Keyboard",
  props: ["alphabet"],
  components: {
    Key
  },
  data() {
    return {
      alphabetLowerCase: this.alphabet,
      key: ""
    };
  },
  computed: {
    alphabetToLowerCase: function() {
      const alphabetLowerCase = this.alphabetLowerCase.toString().toLowerCase();
      return alphabetLowerCase;
    }
  },
  methods: {
    isCorrect: function(e) {
      console.log(e);
    }
  },
  created() {
    bus.$on("getKey", data => {
      this.key = data;
      console.log(this.key);
    });
  }
};
</script>

<style lang="scss" scoped>
.keyboard {
  display: grid;
  grid-template-columns: repeat(7, 100px);
  grid-gap: 10px;
}
</style>
