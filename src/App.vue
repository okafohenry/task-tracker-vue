<template>
  <div class="container">
    <Header />
    <Form />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Form from "@/components/Form";
export default {
  components: {Header, Form}
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
    border-radius: 3px;
    padding: 20px;
  }
</style>
