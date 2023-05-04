<template>
  <form-window :formTitle="`Недостаточно данных`">
    <!-- <div style="display: flex; justify-content: center;"> -->
      <div v-for="(symptom, index) in patientData.symptoms" :key="index" style="width: 80%;">
        <div style="display: flex;" v-if="symptom.value.length === 0">
          <form-label>{{ symptom.name }}</form-label>
          <form-input type="text" v-model=symptom.value />
          <form-select v-model=symptom.dataAccuracy :options="selectOptions" />
          <form-label>Нет данных</form-label>
        </div>

      </div>
    <div style="display: flex; justify-content: center;" >
      <form-button type="button">Отправить</form-button>
      <form-button type="button">Помощь</form-button>
    </div>
  </form-window>
</template>

<script>
import FormWindow from './UI/FormWindow.vue';
import FormButton from './UI/FormButton.vue'
import FormLabel from './UI/FormLabel.vue';
import FormInput from './UI/FormInput.vue';

export default {
  components: {FormWindow, FormButton, FormLabel, FormInput},
  data() {
    return {
      dataSelect: '',
      pulse: {
        pulseValue: '',
        pulseRole: 'exactly'
      },
      selectOptions: [
        {value: '1', name: 'точно'},
        {value: '2', name: 'неточно'},
        {value: '3', name: 'неизмеримо'},
      ]
    }
  },
  props: {
    patientData: {
      type: Object,
    }
  }
}
</script>

<style lang="scss" scoped>
.symptoms{
  width: 70%;

}
</style>