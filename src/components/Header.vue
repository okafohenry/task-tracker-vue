<template>
  <header>
    <h1>Task Tracker</h1>
    <Button text="close" color="#fff" background="red" padding="10px 30px"  />
  </header>
</template>

<script>
import Button from "@/components/Button";
export default {
  name: "Header",
  components: {Button},
  // components: {Button}
}
</script>

<style scoped>
  header{
    display: flex;
    justify-content: space-between;
    padding: 5px 7px;
  }
  h1{
    padding: 0;
    margin: 0;
    font-size: 25px;
    font-weight: 600;
  }
</style>