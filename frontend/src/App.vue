<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <header>
      <h1>{{ msg }}</h1>
  </header>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Events></Events>
  <DynamicStyle></DynamicStyle>
  <VueCourseGoal></VueCourseGoal>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Events from "@/components/Events";
import DynamicStyle from "@/components/DynamicStyle";
import VueCourseGoal from "./components/VueCourseGoal";
export default {
  name: 'App',
  data() {
    return {
      msg: 'Vue JS APP'
    }
  },
  components: {
    HelloWorld,
    Events,
    DynamicStyle,
    VueCourseGoal
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
