<template>
  <img alt="Vue logo" src="./assets/images/meow.jpg" width="300" height="300">
  <Hello msg="냥희진 왈 : 오늘의 날씨는 더움."/>
  <p></p>
  종: {{ kind }}<br>
  고양이를 사랑하는만큼 눌러주세용: {{ info }}<br>
  카운트 :{{ count }}<p></p>
  <button @click="suIncrement">증가(+1)</button>
  <button @click="suDecrement">하락(-1)</button> &nbsp;

  <h3>고양이 하루살이</h3>
  <hr color="#276e7a" size="3">
</template>

<script>
import Hello from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    Hello
  },
  data() {
    return {
      kind: '로드캣(코리안숏헤어)',
      count : 1004,
      info: '고양이를 사랑하는만큼 눌러주세용'
    }
  },

  methods:{
    suIncrement(){
      this.count = this.count+1;
      this.info = this.count;
    },
    suDecrement(){
      this.count = this.count-1;
      this.info = this.count;
    },

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
