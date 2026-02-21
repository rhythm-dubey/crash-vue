<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- <FirstComponent /> -->
  <!-- <ConditionalComponent /> -->
  <!-- <PropertiesComponent /> -->
  <ParentComponent />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import FirstComponent from './components/FirstComponent.vue'
// import ConditionalComponent from './components/ConditionalComponent.vue'
// import PropertiesComponent from './components/PropertiesComponent.vue'
import ParentComponent from './components/ParentComponent.vue'

export default {
  name: 'App',
  components: {
    // FirstComponent
    // ConditionalComponent
    // PropertiesComponent
    ParentComponent
    // HelloWorld
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
