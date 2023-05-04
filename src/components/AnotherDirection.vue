<template>
  <form-window :formTitle="`Другое направление`">
    <div class="directions" v-for="(radioOption) in radioOptions" :key="radioOption.value">
      <input type="radio" v-bind:value="radioOption.value" v-model="direction" />
      <form-label>{{ radioOption.name }}</form-label>
    </div>
    <form-button type="button">Отправить</form-button>
  </form-window>
</template>

<script>
import FormWindow from './UI/FormWindow.vue';
import FormButton from './UI/FormButton.vue';
import FormLabel from './UI/FormLabel.vue';

export default {
  components: {FormWindow, FormButton, FormLabel},
  data() {
    return {
      direction: '',
      radioOptions: [
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