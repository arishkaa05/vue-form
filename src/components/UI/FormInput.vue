<template>
  <input :value="modelValue" @input="updateInput" class="input" type="text" />
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
.input {
  padding: 10px;
  width: 100%;
  background: #FAFAFA;
  border: 1px solid rgb(60, 58, 114);
  margin: 15px 15px 0 0;
  min-width: 40px;
  height: 15px;
}.input:focus {
  border: 2px solid rgb(60, 58, 114);
}
</style>
