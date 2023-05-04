<template>
  <div class="simptoms">
    <div v-for="(symptom, index) in symptoms" :key="index">
      <div style="display: flex;">
        <form-label class="simptom__name">{{ symptom.name }}</form-label>
        <form-input
          type="text"
          v-model="symptom.value"
        />
        <form-select v-model="selectedData" :options="selectOptions" />
      </div>
    </div>
  </div>



</template>

<script>
import FormInput from './UI/FormInput.vue';
import FormSelect from './UI/FormSelect.vue';
import FormLabel from './UI/FormLabel.vue'

export default {
  components: { FormInput, FormSelect, FormLabel },
  data() {
     return {
      props: {
        formSubmitted: {
          type: Boolean,
          default: false
        }
      },
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
      ],
      controls: [],
   }
}}
</script>

<style lang="scss" scoped>

  .simptoms {
    margin-top: 30px;
    width: 60%;
    margin-bottom: 20px;
  }
  .simptom {
    display: flex;
    justify-content: space-between;

  }
</style>