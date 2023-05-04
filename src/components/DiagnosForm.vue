<template>
  <form-window :formTitile="`Предположительный диагноз`">
    <div class="diagnoses">Диагноз:<br><br>
      Лечение: <span class="diagnoses__description">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Fugiat ipsa perferendis accusamus. Voluptatibus ea id doloribus placeat dignissimos tempore amet hic porro quod eos, perspiciatis velit mollitia similique sed vel!</span>
    </div>
    <form-button type="button" @click="$emit('diagnoseSubmit', diagnoseSubmit=true)">Неверный диагноз</form-button>
  </form-window>
</template>

<script>
import FormWindow from './UI/FormWindow.vue';
import FormButton from './UI/FormButton.vue'

export default {
  components: {FormWindow, FormButton},
  data() {
    return {
      diagnoseSubmit: false

    }
  }
}
</script>

<style lang="scss" scoped>
  .diagnoses {
    font-size: 16px;
    color: #3d3d3dd1;
    font-weight: 600;
    width: 80%;
    margin: 20px 0 20px;
    &__description {
      font-size: 14px;
      font-weight: 200;
    }
  }
</style>