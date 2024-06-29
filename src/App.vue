<template>
  <div>
  <img alt="Vue logo" src="./assets/images/meow.jpg" width="300" height="300">
  <Hello msg="냥희진 왈 : 오늘의 날씨는 더움."/>
  <p></p>
  종: {{ kind }}<br>
  카운트 :{{ count }}<p></p>

  <h3>고양이 리스트</h3>
  <hr color="#276e7a" size="3">

  <BoardTest/>
  </div>
</template>

<script>
// import Hello from './components/HelloWorld.vue'
import BoardTest from './components/BoardTest.vue'

export default {
  name: 'App',
  components: {
    BoardTest,
  },
  data() {
    return {
      kind: '로드캣(코리안숏헤어)',
      count : 1004,
      info: '클릭클릭클릭',
// 게스트 guest:[name,age,title]
      guest:[
      {name:'meow',age:3,title:'coco'},
      {name:'meooow',age:6,title:'장군이'},
      {name:'냥',age:7,title:'juhaneeee'}
      ],
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

#button {
  background-color: #276e7a;
  border: none;
  border-radius: 10px;
  color: white;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 16px 2px;
  cursor: pointer;
  transition: background-color 0.3s ease; /* 배경색 변화를 부드럽게 만듦 */
}

#button:hover {
  background-color: #3a8999; /* 마우스를 올렸을 때 색상 변경 */
}

#index {
  background-color: #f0f0f0;
  padding: 10px;

  border-radius: 5px;
}

hr {
  border-color: #ffffff;
  margin-top: 5px;
  margin-bottom: 5px;
}

</style>