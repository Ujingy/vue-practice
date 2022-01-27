<template>
  <h2>handsome? {{ isHandsome }}</h2>
  <h3>{{ name }}</h3>
</template>

<script>
// import { reactive, toRefs } from "vue";
import { ref, reactive, toRefs } from "vue";
export default {
  name: "TestComponent",
  setup() {
    let isHandsome = ref(false);
    const state = reactive({
      name: "Ujing",
      age: 50,
      job: "programmer",
    });
    // let isNotUgly = isHandsome;
    // isHandsome.value = true;
    // console.log(isNotUgly);
    return {
      isHandsome,
      ...toRefs(state),
    };
    // const state = reactive({
    //   username: "Ujing",
    //   age: 50,
    // });
    // return toRefs(state);
  },
  //   data() {
  //     return {
  //       username: "Ujing",
  //     };
  //   },
};
</script>

<style></style>
