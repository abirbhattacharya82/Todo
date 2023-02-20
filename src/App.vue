<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <MainContainer/>
</template>

<script>
import MainContainer from './components/MainContainer/MainContainer.vue'
export default {
  name: 'App',
  components: {
    MainContainer
  }
}
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  margin-top: 5%;
  width: 100%;
}
</style>
