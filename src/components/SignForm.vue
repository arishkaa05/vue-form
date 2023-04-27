<template>
  <form @submit.prevent="$emit('formSubmit', formSubmitted=true)">
    <div class="identification">
      <label class="identification__label">ФИО</label>
      <input type="text" required v-model="name">
    </div>
    <div class="identification">
      <label class="identification__label">№</label>
      <input type="text" required v-model="identification">
    </div>
    <div class="simptoms">
      <div class="simptom">
        <label class="simptom__name">Пульс</label>
        <input class="simptom__input" type="text" v-model="pulse.pulseValue">
        <select class="simptom__select" v-model="pulse.pulseRole">
          <option value="exactly" selected>Точные данные</option>
          <option value="not-exactly">Неточные данные</option>
          <option value="impossibility">Невозможно измерить</option>
        </select>
      </div>
      <div class="simptom">
        <label class="simptom__name">Давление</label>
        <input class="simptom__input" type="text" v-model="pressure.pressureValue">
        <select class="simptom__select" v-model="pressure.pressureRole">
          <option value="exactly" selected>Точные данные</option>
          <option value="not-exactly">Неточные данные</option>
          <option value="impossibility">Невозможно измерить</option>
        </select>
      </div>
    </div>
    <button type="submit">Отправить</button>
  </form>

</template>

<script>
export default {
  data() {
    return {
      name: '',
      formSubmitted: false,
      identification: '',
      pulse: {
        pulseValue: '',
        pulseRole: 'exactly'
      },
      pressure: {
        pressureValue: '',
        pressureRole: 'exactly'
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  form {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
  }
  label {
    color: #aaa;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  input {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color:#555;
  }
  button {
    padding: 10px 40px;
    border: 1px solid #9a9a9a;
    border-radius: 7px;
    color: #222;
    cursor: pointer;
    margin: 20px 35%;
  }
  input:hover {
    outline: none;
  }
  .identification {
    display: flex;
    &__label {
      width: 60px;
    }
  }
  .simptoms {
    margin-top: 70px;
    margin-bottom: 40px;
  }
  .simptom {
    display: flex;
    justify-content: space-between;
    &__name {
      width: 20%;
    }
    &__input {
      margin: 0 20px;
      width: 30%;
      border-bottom: 1px solid #ddd;
    }
    &__select {
      color:#555;
      border: none;
      border-bottom: 1px solid #ddd;
    }
  }
</style>