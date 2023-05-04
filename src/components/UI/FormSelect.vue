<template>
  <select class="select" :value="modelValue" @change="changeOption">
    <option disabled value="">Выберите</option>
    <option v-for="option in options" :key="option.value" :value="option.value">
      {{ option.name }}
    </option>
  </select>
</template>

<script>
export default {
  name: "FormSelect",
  props: {
    modelValue: {
      type: String,
    },
    options: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    changeOption(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
.select {
  margin-top: 15px;
  padding: 10px 15px;
  background: none;
  color: rgb(60, 58, 114);;
  border: 1px solid rgb(60, 58, 114);
}
</style>
