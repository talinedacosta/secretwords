<template>
  <button
    class="key"
    :class="isCorrect"
    :disabled="isDisabled"
    @click.prevent="handleClick"
  >
    <slot></slot>
  </button>
</template>

<script>
import { bus } from "@/main.js";

export default {
  name: "Key",
  data() {
    return {
      isDisabled: false,
      isCorrect: null
    };
  },
  methods: {
    handleClick: function() {
      const key = event.target.innerHTML;
      this.isDisabled = true;

      bus.$emit("getKey", key);
    }
  }
};
</script>

<style lang="scss" scoped>
button {
  border-radius: 5px;
  border: none;
  background: #aa9ad9;
  color: #ffffff;
  font-size: 20px;
  text-align: center;
  padding: 10px 0;
  text-transform: uppercase;
  transition: all 0.8s;

  &.correct {
    background: #c4a1e3;
  }

  &.not-correct {
    background: grey;
    color: white;
  }
}
</style>
