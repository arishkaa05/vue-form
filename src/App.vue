<template>
   <div id="app" class="app">
    <SignForm @formSubmit="formSubmit"/>
    <DiagnosForm v-if="formSubmitted" @diagnoseSubmit=diagnoseSubmit />
    <MedicalDirection v-if="diagnoseInCorrect" @diagnoseDirection="diagnoseDirection"/>
    <AddExamination  v-if="this.diagnoseValue==1"/>
    <AnotherDirection v-if="this.diagnoseValue==2"/>
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
   },
   data: () => ({
    formSubmitted: false,
    diagnoseInCorrect: false,
    diagnoseValue: 0,
   }),
   methods: {
    formSubmit() {
      this.formSubmitted = !this.formSubmitted
    },
    diagnoseSubmit() {
      this.diagnoseInCorrect = !this.diagnoseInCorrect
    },
    diagnoseDirection(value) {
      this.diagnoseValue = value
    }
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
