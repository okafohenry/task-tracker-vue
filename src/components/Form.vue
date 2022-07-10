<template>
  <form>
    <label htmlFor="task">Task</label><br/>
    <input type="text" id="task" placeholder="Add Task" /><br/>
    <label htmlFor="day-time">Day & Time</label><br/>
    <input type="datetime-local" id="day-time" placeholder="Add Day & TIme" /><br/>
    <div class="checkbox">
      <label>Set Reminder</label>
      <input type="checkbox" />
    </div>
    <button class="btn" type="submit"> Save Task </button>

  </form>
</template>
<script>
import Button from "@/components/Button";
export default {
  components: {Button}
}
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