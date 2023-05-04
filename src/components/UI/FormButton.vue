<template>
  <div style="display: flex; justify-content: center;">
    <button><slot></slot></button>
  </div>

</template>

<script>
export default {
  name: "FormInput",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput() {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
button {
  padding: 8px 20px;
  border: 1px solid rgb(60, 58, 114);
  background: #fafafa;
  color: #3d3d3dd1;
  font-weight: 600;
  margin: 15px;
}
button:focus {
  border: 2px solid rgb(60, 58, 114);
}
</style>
