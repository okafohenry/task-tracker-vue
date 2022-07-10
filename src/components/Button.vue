<template>
  <div>
    <button :style="{color, background, padding}">{{ text }}</button>
  </div>
</template>
<script>
 export default {
   name: "Button",
   props: {
     text: String,
     color: String,
     background: String,
     padding: String,
   }
 }
</script>
<style scoped>
  button{
    border: none;
    font-size: 14px;
    letter-spacing: 1px;
    border-radius: 5px;
  }
</style>