<template>
  <buttonComponent modelValue="Je suis un bouton" />
  <div v-for="button in buttons" :key="`button${button.id}`">
    <buttonComponent :modelValue="button.text" />
  </div>
</template>

<script>
import buttonComponent from './components/btn_component.vue'

export default {
  name: 'App',
  components: {
    buttonComponent
  },
  data() {
    return {
      buttons: [
        {"id": 1, "text": "Cliquer ici"},
        {"id": 2, "text": "Cliquer là"},
      ]
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
</style>
