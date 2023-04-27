<template>
  <div class="diagnos">
    <div class="diagnos__name">Кардиология</div>
    <div style="display: flex; justify-content: space-around;" >
      <button type="button">Да</button>
      <button type="button">Нет</button>
    </div>
    <div style="display: flex; justify-content: center;">
      <button type="button">Помощь</button>
    </div>
  </div>

</template>

<script>
export default {
  data() {
    return {

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
</style>