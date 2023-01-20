<template>
  <h2>Username: {{ name }}</h2>
  <h3>Age: {{ age }}</h3>
</template>

<script>
export default {
  props: ["name", "age"],
  data() {},
};
</script>
