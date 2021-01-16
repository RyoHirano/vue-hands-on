<template>
  <button @click="onCountUpClick">+1</button>
  <div>Click Count: {{ state.count }}</div>
</template>

<script>
import { reactive } from "vue";
export default {
  setup() {
    const state = reactive({
      count: 0,
    });
    const onCountUpClick = () => state.count++;
    return {
      state,
      onCountUpClick,
    };
  },
};
</script>
