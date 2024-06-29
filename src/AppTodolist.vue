<template>
    <div class="todo-list">
      <h2>할일 목록</h2>
      
      <!-- 할일 추가 폼 -->
      <form @submit.prevent="addTodo">
        <input type="text" v-model="newTodo" placeholder="할일 추가">
        <button type="submit">추가</button>
      </form>
      
      <!-- 할일 목록 -->
      <ul>
        <li v-for="(todo, index) in todos" :key="index">
          {{ todo }}
          <button @click="removeTodo(index)">삭제</button>
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        newTodo: '', // 입력 폼에 입력된 새로운 할일
        todos: []    // 할일 목록 배열
      };
    },
    methods: {
      // 할일 추가 메서드
      addTodo() {
        if (this.newTodo.trim() !== '') {
          this.todos.push(this.newTodo.trim()); // 새로운 할일을 배열에 추가
          this.newTodo = ''; // 입력 폼 초기화
        }
      },
      // 할일 삭제 메서드
      removeTodo(index) {
        this.todos.splice(index, 1); // 인덱스에 해당하는 할일 삭제
      }
    }
  };
  </script>
  
  <style scoped>
  .todo-list {
    font-family: 'Noto Sans KR', sans-serif; /* 폰트 설정 */
    width: 300px;
    margin: auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  form {
    margin-bottom: 10px;
  }
  
  input[type="text"] {
    padding: 8px;
    width: 200px;
    margin-right: 10px;
  }
  
  button {
    padding: 8px 16px;
    background-color: #276e7a;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #3a8999;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    margin-bottom: 5px;
  }
  </style>