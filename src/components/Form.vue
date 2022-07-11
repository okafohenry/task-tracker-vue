<template>
  <form @submit="handleSubmit()">
    <div>
      <label>Task</label><br/>
      <input type="text" v-model="task" id="task" placeholder="Add Task" />
    </div>
    <div>
      <label>Day & Time</label><br/>
      <input type="datetime-local" v-model="day" id="day-time" placeholder="Add Day & TIme" />
    </div>
    <div class="checkbox">
      <label>Set Reminder</label>
      <input type="checkbox" v-model="reminder" />
    </div>
    <button class="btn" @click="handleClick()"> Save Task </button>
  </form>
</template>
<script>
  import Button from "@/components/Button";
  export default {
    components: {Button},
    methods: {
      handleClick(event) {
        event.preventDefault();
        console.log("logged!");
      }
    },
    data(){
      return{
        task: '',
        day: '',
        reminder: false
      }
    }
  };
</script>
<style scoped>
  form{
    max-width: 90%;
  }
  input{
    width: 100%;
    padding: 10px;
  }
  button{
    max-width: 400px;
    width: 107%;
    padding: 10px;
    background: #000;
    border: none;
    color: #fff;
  }
  div{
    margin-top: 15px;
  }
  .checkbox{
    display: flex;
    font-size: 13px;
    padding: 10px 0;
    gap: 3rem;
  }
  .checkbox input{
    width: 14px;
    height: 14px;
  }
</style>