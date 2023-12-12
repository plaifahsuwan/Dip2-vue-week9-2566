<template>
  <div>
    <img src="./assets/logo.png" alt="Vue logo">
    <!-- static props -->
    <greeting-message first-name="Mark" last-name="Zuckerberg" />
    <greeting-message first-name="Elon" last-name="Musk" />
    <greeting-message first-name="Leo" last-name="Messi" />
    <hr />
    <!-- Dynamic props -->
    <greeting-message :first-name="fName" :last-name="lName" />
    <greeting-message :full-name="fullName" />

  </div>
</template>

<script>
import GreetingMessage from './components/GreetingMessage.vue';
export default {
  name: 'App',
  components: {
    GreetingMessage,
  },
  data() {
    return {
      fName: 'Jhon',
      lName:'Doe',
    }
  },
  computed: {
    fullName() {
      return this.fName + " " + this.lName
    }
  },
}
</script>

<style>
#app {
  text-align: center;
}
</style>