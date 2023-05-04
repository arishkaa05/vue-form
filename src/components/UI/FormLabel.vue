<template>
  <label><slot></slot></label>
</template>

<script>
export default {
  name: "FormLabel",
};
</script>

<style scoped>
label {
    min-width: 80px;
    font-size: 12px;
    margin: 25px 20px 0 0;
    color: #3d3d3dd1;
    font-weight: 600;
}

</style>
