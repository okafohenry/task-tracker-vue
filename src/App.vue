<template>
  <div class="container">
    <Header />
    <Form />
    <Task @deleteTask="handleTaskDelete" :tasks="tasks" />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Form from "@/components/Form";
import Task from "@/components/Task";

export default {
  components: {Header, Form, Task},
  data(){ // react-state equivalent
    return {
      tasks: []
    }
  },

  methods: {
    handleTaskDelete(id){
      this.tasks = this.tasks.filter(item => item.id !== id);
    }
  },
  created(){
    this.tasks = [
      {
        id: 1,
        text: "Doctors appointment",
        day: "May 1st, 2:30pm",
        reminder: true
      },
      {
        id: 2,
        text: "Live Coding Session",
        day: "May 1st, 2:30pm",
        reminder: true
      },
      {
        id: 3,
        text: "food Shopping",
        day: "May 1st, 2:30pm",
        reminder: true
      },
    ]
  },


}
</script>

<style>
  #app{
    font-family: "Lucida Sans";
  }
  .container{
    width: 27%;
    margin: 0 auto;
    border: 1px solid #787878;
    padding: 30px;
  }
</style>
