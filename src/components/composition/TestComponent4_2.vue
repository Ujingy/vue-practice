<template>
  <h2>Hello LifeCycle</h2>
  <ChildComponent firstname="Code" lastname="Ujing" @sendParent="sendParent" />
</template>

<script>
import ChildComponent from "./ChildComponent.vue";
import {} from "vue";
export default {
  name: "TestComponent",
  components: { ChildComponent },
  methods: {
    sendParent() {
      console.log("parent event!!!");
    },
  },
};
</script>

<style></style>
