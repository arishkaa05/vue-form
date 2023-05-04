<template>
  <form-window :formTitle="`Введите данные`">
      <div style="display: flex;">
        <form-label class="identification__label">ФИО</form-label>
        <form-input type="text" placeholder="Иванов Иван Иванович" required v-model="name" />
      </div>
      <div style="display: flex;">
        <form-label class="identification__label">№</form-label>
        <form-input type="text" placeholder="653683468" required v-model="identification" />
      </div>
      <div class="diagnosis">
        <div class="symptoms">
          <div v-for="(symptom, index) in symptoms" :key="index">
            <div style="display: flex;">
              <form-label class="simptom__name">{{ symptom.name }}</form-label>
              <form-input
                type="text"
                v-model="symptom.value"
              />
              <form-select v-model="symptom.dataAccuracy" :options="selectOptions" />
            </div>
          </div>
        </div>
        <!-- <div  class="diagnos">
          Предположительный диагноз
          <table>
            <tr>
              <td style="border: 1px solid gray;">{{ name }}</td>
              <td style="border: 1px solid gray;">{{ identification }}</td>
            </tr>
            <tr v-for="(symptom, index) in symptoms" :key="index">
              <td style="border: 1px solid gray; min-width: 20px;">{{ symptom.name }}</td>
              <td style="border: 1px solid gray; min-width: 20px;">{{ symptom.value }}</td>
              <td style="border: 1px solid gray; min-width: 20px;">{{ symptom.dataAccuracy }}</td>
            </tr>
          </table>
        </div> -->
      </div>
      <form-button type="submit" @click="this.$emit('formSubmit', {
      name: this.name,
      identification: this.identification,
      symptoms: this.symptoms
    })"> Отправить</form-button>
  </form-window>
</template>

<script>
import FormInput from './UI/FormInput.vue';
import FormWindow from './UI/FormWindow.vue';
import FormLabel from './UI/FormLabel.vue'
import FormSelect from './UI/FormSelect.vue';
import FormButton from './UI/FormButton.vue'



export default {
  components: { FormWindow, FormInput, FormLabel, FormSelect, FormButton },
  data() {
    return {
      name: ' ',
      identification: ' ',
      symptoms: [
        {
          name: 'Пульс',
          value: '',
          dataAccuracy: '',
          pattern: /^[0-9]+$/
        },
        {
          name: 'Давление',
          value: '',
          dataAccuracy: '',
          pattern: /^[0-9]+$/
        },
        {
          name: 'Температура',
          value: '',
          dataAccuracy: '',
          pattern: /^[0-9]+$/
        },
        {
          name: 'Мимика лица',
          value: '',
          dataAccuracy: '',
          pattern: /^[0-9]+$/
        },
        {
          name: 'КГР',
          value: '',
          dataAccuracy: '',
          pattern: /^[0-9]+$/
        },
        {
          name: 'Открытость глаз',
          value: '',
          dataAccuracy: '',
          pattern: /^[0-9]+$/
        },
        {
          name: 'Качество сна',
          value: '',
          dataAccuracy: '',
          pattern: /^[0-9]+$/
        }
      ],
      selectOptions: [
        {value: '1', name: 'точно'},
        {value: '2', name: 'неточно'},
        {value: '3', name: 'неизмеримо'},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.symptoms {
  //margin-top: 30px;
  width: 60%;
  margin-bottom: 40px;
}
.simptom {
  display: flex;
  justify-content: space-between;

}
.diagnosis {
  display: flex;
  margin-top: 30px;
  font-weight: 600;
  color: #3d3d3dd1;
}
.diagnos {
  margin: 15px;
}
</style>