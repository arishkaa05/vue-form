<template>
   <form>
    <div>Picked: {{ picked }}</div>

    <input type="radio" id="one" value="One" v-model="picked" />
    <label for="one">One</label>

    <input type="radio" id="two" value="Two" v-model="picked" />
    <label for="two">Two</label>
    <div class="direction">
      <input type="radio" class="direction__inactive" checked>
      <label>Кардиология</label>
    </div>
    <div class="direction">
      <input type="radio" >
      <label>Неврология</label>
    </div>
    <div class="direction" >
      <input type="radio" v-model="checked">
      {{ checked }}
      <label>Иное</label>
    </div>
    <select class="simptom__select">
      <option value="exactly" selected>Офтальмология </option>
      <option value="not-exactly">Эндокринология</option>
    </select>


  </form>
</template>

<script>
export default {
  data() {
    return {
      anotherActive: false
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
    color:#555;
    font-size: 16px;
  }
.direction{
  margin: 0 10px;
  &__inactive{
    color: #ccc;
  }
}
.simptom {
    &__select {
  margin: 5px 10px;
      border: none;
      border-bottom: 1px solid #ddd;
      color:#555;
      font-size: 16px;
    }
  }
</style>