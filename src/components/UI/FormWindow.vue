<template>
  <div class="form">
    <div class="form__content">
      <h2 class="form__title">{{ formTitle }}</h2>
      <slot></slot>
   </div>
  </div>

</template>

<script>
export default {
  name: "FormWindow",
  props: {
    formTitle: {
      type: String,
      required: true
    }
  },
};
</script>

<style scoped lang="scss">
.form {
  margin: 60px auto;
  padding: 20px 40px;
  background: #fafafa;
  min-height: 177px;
  width: 720px;
  &__title{
    color: #3d3d3d;
    font-weight: 600;
    text-align: center;
  }
}

</style>
