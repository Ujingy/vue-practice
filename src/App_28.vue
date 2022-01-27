<template>
  <div>
    <h2>Hello Ref</h2>
    <ParentComp />
  </div>
</template>

<script>
import ParentComp from "./components/lifecycle/ParentComp";
export default {
  name: "App",
  components: { ParentComp },
  data() {
    return {};
  },
};
</script>

<style></style>
