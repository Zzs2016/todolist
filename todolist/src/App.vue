<template>
  <div id="app">
    <h1>ToDoList</h1>
    <input ref="add_something" v-model="todoField" @keyup.enter="addTodo" placeholder="do something..."/>
    <ul>
      {{ todoField }}
       <!--<li v-for="todoItem in todoList" :todoItem="todoItem"></li>
    -->
    </ul>
  </div>
</template>

<script>
import ToDo from './components/ToDo'
import VueResource from 'vue-resource'
export default {
  name: 'App',
  components:{
    ToDo
  },
  data(){
    // something = this.$refs.add_something.value
    return {
      todoField: ''
    }
  },
  // computed: {
  //   todoList(){
  //   return this.todos
  //   }
  // }
  methods: {
    addTodo: function(){
        alert('asddfdf')
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
