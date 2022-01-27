<template>
  <h2>Hello LifeCycle</h2>
  <input type="text" v-model="username" ref="inputRef" />
</template>

<script>
import {
  ref,
  // onBeforeMount,
  onMounted,
  // onBeforeUpdate,
  // onUpdated,
  // onBeforeUnmount,
  // onUnmounted,
} from "vue";
export default {
  name: "TestComponent",
  setup() {
    const inputRef = ref(null);
    const username = ref("Ujing");
    // onBeforeMount(() => {
    //   console.log("onBeforeMount");
    // });
    onMounted(() => {
      inputRef.value.focus();
      console.log("onMounted");
    });
    // onBeforeUpdate(() => {
    //   console.log("onBeforeUpdate");
    // });
    // onUpdated(() => {
    //   console.log("onUpdated");
    // });
    // onBeforeUnmount(() => {
    //   console.log("onBeforeUnmount");
    // });
    // onUnmounted(() => {
    //   console.log("onUnmounted");
    // });
    return {
      username,
      inputRef,
    };
  },
};
</script>

<style></style>
