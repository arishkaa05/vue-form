<template>
  <div class="diagnos">
    Диагноз:
    <button type="button">Неверный диагноз</button>
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
    margin: 10px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
  }
  button {
    padding: 10px 40px;
    border: 1px solid #9a9a9a;
    border-radius: 7px;
    color: #555;
    margin: 20px 35%;
  }
</style>