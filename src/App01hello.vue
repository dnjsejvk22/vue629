<template>
  <img alt="Vue logo" src="./assets/images/meow.jpg" width="300" height="300">
  <HelloWorld msg="냥희진 왈 : 오늘의 날씨는 더움."/>

  <h3>testing 쉬는시간</h3>
  <hr color="#276e7a" size="3">
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #276e7a;
}
</style>
