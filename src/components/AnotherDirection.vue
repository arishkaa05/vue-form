<template>
   <form>
    <div id="v-model-radiobutton">
    <input type="radio" id="one" value="1" v-model="picked" />
    <label for="one">Неврология</label>
    <br />
    <input type="radio" id="two" value="2" v-model="picked" />
    <label for="two">Офтальмология</label>
    <br />
    <input type="radio" id="three" value="3" v-model="picked" />
    <label for="three">Иное</label>
    <br />
    <div v-if="picked==3">
      <select class="simptom__select">
        <option value="1">Эндокринология</option>
        <option value="2">Дермотология</option>
        <option value="3">Педиатрия</option>
      </select>
    </div>
  </div>


  </form>
</template>

<script>
export default {
  data() {
    return {
      picked: ''
    }
  },
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
label {
     color: #999;
    // display: inline-block;
    // margin: 25px 0 15px;
     font-size: 12px;
     text-transform: uppercase;
     letter-spacing: 1px;
     font-weight: bold;
     margin-bottom: 10px;
  }
input {
    //display: block;
     padding: 10px 16px;
    // width: 100%;
    // box-sizing: border-box;
    // border: none;
    // border-bottom: 1px solid #ddd;
     color:#555;
  }
.simptom {
    &__select {
      margin: 5px 10px;
      border: none;
      border-bottom: 1px solid #ddd;
      color:#999;
      font-size: 16px;
    }
  }
</style>