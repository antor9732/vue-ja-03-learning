<!-- <script >
export default {
  data() {
    return {
      awesome: 'Antor',
      vShowState: false,
    }
  },
  methods: {
    toggle(value) {
      this.awesome = value;
    },
    toggleShow() {
      this.vShowState = !this.vShowState;
    }
  }
}
</script>

<template>
<h1 v-show="vShowState">Hello!</h1>

<button @click="toggleShow">TOGGLE SHOW</button>
<br>

  <template v-if="awesome == 'Antor'">
    <h1>Conditional Rendering1</h1>
    <h1>Conditional Rendering3</h1>
    <h1>Conditional Rendering4</h1>

  </template>

  <h1 v-if="awesome == 'Antor'">Antor is awesome!</h1>
  <h1 v-else-if="awesome == 'Mahmudul'">Mahmudul is awesome!</h1>
  <h1 v-else>Vue is Super</h1>

  <button @click="toggle('Antor')">TOGGLE to Antor</button>
  <button @click="toggle('Mahmudul')">TOGGLE to Mahmudul</button>
  <button @click="toggle('')">TOGGLE to None</button>

</template>

<style scoped>

</style> -->

<script>
import Form from './components/Form.vue';
import MultiStepForm from './components/MultiStepForm.vue';
import Header from './components/Header.vue';


export default {
  components: {
    Header,
    Form,
    MultiStepForm,
  },
}
</script>

<template>
  <!-- <Header /> -->
   <!-- <Form /> -->
    <MultiStepForm/>

</template>

<style scoped></style>
