<template>
  <div class="wrapper">
    <div :key="task.id" v-for="task in tasks" class="task">
      <h3>
        {{task.text}}
      <i class="fas fa-times" @click="handleDelete(task.id)"></i>
      </h3>
      <p>{{task.day}}</p>
    </div>
  </div>
</template>
<script>
  export default{
    name: "Task",
    props: {
      tasks: Array
    },
    methods: {
      handleDelete(item){
        this.$emit('deleteTask', item)
      }
    }
  }
</script>
<style scoped>
  .wrapper{
    overflow-y: auto;
    padding: 0;
    margin-top: 15px;
    width: 97%;
    height: 200px;
    border: none;
  }
  .wrapper::-webkit-scrollbar{
    width: 5px;
  }
  .task{
    background: #f4f4f4;
    padding: 10px 20px;
    margin-top: 1px;
  }
  h3{
    font-size: 16px;
    display: flex;
    justify-content: space-between;
    margin: 0;
    padding: 0;
    line-height: 16px;
  }
  .fas{
    cursor: pointer;
  }
  p{
    font-size: 14px;
    line-height: 0;
  }
  .active{
    border-left: 2px solid forestgreen;
  }

</style>