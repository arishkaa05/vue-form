<template>
  <form-window :formTitile="`Направление`">
    <div class="diagnos" @click="$emit('diagnoseDirection', this.diagnoseDirection)">
      <div class="diagnoses__name">Кардиология</div>
      <div style="display: flex; justify-content: center;" >
        <form-button type="button" @click="diagnoseDirection=1">Да</form-button>
        <form-button type="button" @click="diagnoseDirection=2">Нет</form-button>
      </div>
      <div style="display: flex; justify-content: center;">
        <form-button type="button" @click="diagnoseDirection=3">Помощь</form-button>
      </div>
    </div>
  </form-window>
</template>

<script>
import FormWindow from './UI/FormWindow.vue';
import FormButton from './UI/FormButton.vue'

export default {
  components: {FormWindow, FormButton},
  data() {
    return {
      diagnoseDirection: 0,
    }
  }
}
</script>

<style lang="scss" scoped>
.diagnoses {
  &__name {
    font-size: 32px;
    text-align: center;
    color: #3d3d3dd1;
    font-weight: 600;
    margin-bottom: 20px;
  }
}
</style>