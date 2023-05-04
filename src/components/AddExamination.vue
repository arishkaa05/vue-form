<template>
  <form-window :formTitile="`Недостаточно данных`">
    <div class="diagnos">
        <div class="simptom">
          <div style="display: flex;">
            <form-label class="simptom__name">Пульс</form-label>
            <form-input class="simptom__input" type="text" v-model="pulse.pulseValue" />
            <form-label>Нет данных</form-label>
          </div>

        </div>
      <div style="display: flex; justify-content: space-around;" >
        <form-button type="button">Отправить</form-button>
        <form-button type="button">Помощь</form-button>
      </div>
    </div>
  </form-window>
</template>

<script>
import FormWindow from './UI/FormWindow.vue';
import FormButton from './UI/FormButton.vue'
import FormLabel from './UI/FormLabel.vue';

export default {
  components: {FormWindow, FormButton, FormLabel},
  data() {
    return {
      pulse: {
        pulseValue: '',
        pulseRole: 'exactly'
      },
    }
  }
}
</script>

<style lang="scss" scoped>

</style>