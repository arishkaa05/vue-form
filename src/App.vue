<template>
  <SignForm />
</template>
<script>

import SignForm from './components/SignForm.vue';

export default {
  name: 'App',
  components: {
    SignForm,
   }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  background: #eee;
  margin: 0;
}
</style>
