<template>
   <div id="app" class="app">
    <SignForm />
    <DiagnosForm />
    <MedicalDirection />
    <AddExamination />
    <AnotherDirection />
   </div>
</template>

<script>

import SignForm from './components/SignForm.vue';
import DiagnosForm from './components/DiagnosForm.vue';
import MedicalDirection from './components/MedicalDirection.vue';
import AddExamination from './components/AddExamination.vue';
import AnotherDirection from './components/AnotherDirection.vue';


export default {
  name: 'App',
  components: {
    SignForm,
    DiagnosForm,
    MedicalDirection,
    AddExamination,
    AnotherDirection
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
