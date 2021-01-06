<template>
  <view class="container">
    <text class="text-color-primary">todo app</text>
   
 

  <text-input
        :style="{height: 40, width: 200, borderColor: 'gray', borderWidth: 1}"
        placeholder="Type your todo list"   v-model="newTodo"
      />
       <button title="Add todo" @press="addTodo" />
      <text v-for="todo in todos" :key="todo.id">{{todo.id + ""+ todo.text}}</text>

  </view>
</template>

<script>
export default {
  data() {
    return {
      message: "Todo app",
      todos: [
        { id: 1, text: "Learn JavaScript" },
        { id: 2, text: "Learn Vue" },
        { id: 3, text: "Build something awesome" }
      ],
      newTodo: "",

    };
  },


  methods: {
    exclaim() {
      this.message += "!";
    },

    addTodo(){
      alert("hello")

         this.todos.push({
           id: this.todos.length+1,
          text: this.newTodo,
         
        });
        this.newTodo = "";

    }



  },
};


</script>

<style>
.container {
  flex: 1;
  background-color: white;
  align-items: center;
  justify-content: center;
}
.text-color-primary {
  color: blue;
  font-size: 30;
}
</style>