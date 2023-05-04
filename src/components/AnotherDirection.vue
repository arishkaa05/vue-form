<template>
  <form-window :formTitle="`Другое направление`">
    <div class="directions" v-for="(radioOption) in radioOptions" :key="radioOption.value">
      <input type="radio" v-if="radioOption.value !== '0'" v-bind:value="radioOption.value" v-model="direction" />
      <input type="radio" v-else v-bind:value="radioOption.value" v-model="direction" disabled/>
      <form-label class="radio">{{ radioOption.name }}</form-label>
    </div>
    <div>
      <form-input />
    </div>
    <form-button type="button">Отправить</form-button>
  </form-window>
</template>

<script>
import FormWindow from './UI/FormWindow.vue';
import FormButton from './UI/FormButton.vue';
import FormInput from './UI/FormInput.vue';
import FormLabel from './UI/FormLabel.vue';

export default {
  components: {FormWindow, FormButton, FormLabel, FormInput},
  data() {
    return {
      direction: '',
      radioOptions: [
        {value: '0', name: 'Кардиология'},
        {value: '1', name: 'Эндокринология'},
        {value: '2', name: 'Дермотология'},
        {value: '3', name: 'Педиатрия'},
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
</style>