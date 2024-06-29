<template>
  <div class="container">
     <img id="cat" alt="Vue logo" src="./assets/images/meow2.jpg" width="300" height="300"><br><br>
     <div><p id="titleText">"여자가 담배를 핀다는건 그만큼 힘들다는거야.."</p></div><br>
     <input type="text" v-model="todoText" size=15 @keyup.enter="insertTodo">
     <button id="button" @click="insertTodo">todo</button>
     <br><br><hr color="black" size="3">
  <h3>고양이 리스트</h3>
  <hr color="black" size="3"><br>
  <todotest/>
  <Hello ka="~폭스걸 웰컴~"></Hello>
  <div>

        Test.vue 저자:{{name}}
        <div v-for="(item) in todolist" :key="item.id" style="color: black;">
          {{ item.checked }} &nbsp;
          {{ item.id }} &nbsp;
          {{ item.text }} 
    </div>
</div>



  </div>
  <HelloWorld />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
// import BoardTest from './components/BoardTest.vue'

export default {
  name: 'App',
  components:{HelloWorld},

  data() {
    return {
      kind: '로드캣(코리안숏헤어)',
      todoText : 'L.O.V.E',
      count : 1,
// 게스트 guest:[name,age,title]
      todolist:[
      {id:1, name:'meow',text:'hot',checked:false},
      {id:2, name:'oh',text:'cool',checked:true}
      ],
    }
  },
  methods :{
    // export default {
    //   name: 'Todotest',
    //   data(){
    //     return{
    //       lotto: 1,
    //     }
    //   }
    // },
    insertTodo(){
      // alert("똑바로 작성하시오--+");
      var max = this.todolist.reduce(function(a,b){
        console.log("a=",a);
        return a>b ? a : b.id ;
      });

      this.todolist.push({
        id:max+1,
        text:this.todoText,
        checked:false
      });
      this.todoText = ''
    },
    deleteTodo(){
      var max = this.todolist.reduce(function(a,b){
        console.log("a=",a);
        return a>b ? a : b.id ;
      })
      alert('todotest.vue deleteTodo 함수');
    },
    toggleCheakbox(){
      console.log('todotest.vue toggleCheakbox 함수')
      alert('todotest.vue toggleCheakbox 함수')
    
    }
  }
}

</script>

<style>
#cat
{ 
  border: 3px
  solid black
  
}

#titleText{
font-size: large;
}

.container{
  background-color: #00000018;
  padding: 20px;
  width: 400px;
}

#button{
  background-color: black;
  color: #ffffff;
  font-family: 'Noto Sans KR', sans-serif;
}

</style>