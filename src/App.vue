<template>
  <div>
    <h2>进度条</h2>
    <MyProgress :percentage="20" status="warning"></MyProgress>
    <MyProgress :percentage="70" status="normal"></MyProgress>
    <MyProgress status="happy"></MyProgress>
    <MyProgress></MyProgress>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },

  created() {},

  methods: {},
};
</script>

<style scoped></style>
