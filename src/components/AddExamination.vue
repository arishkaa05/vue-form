<template>
  <div class="diagnos">
     <div class="diagnos__name">Недостаточно данных</div>
      <div class="simptom">
        <div style="display: flex;">
          <label class="simptom__name">Пульс</label>
          <input class="simptom__input" type="text" v-model="pulse.pulseValue">
          <label>Нет данных</label>
        </div>

      </div>
    <div style="display: flex; justify-content: space-around;" >
      <button type="button">Отправить</button>
      <button type="button">Помощь</button>
    </div>
  </div>

</template>

<script>
export default {
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
  .diagnos {
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
    &__name {
      font-size: 24px;
      text-align: center;
      margin-bottom: 20px ;
    }
  }
  button {
    padding: 10px 40px;
    border: 1px solid #9a9a9a;
    border-radius: 7px;
    color: #555;
    margin: 20px;
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
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color:#555;
    margin-right: 20px;
  }

</style>