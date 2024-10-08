<template>
    <p>Resultado: {{ result }}</p>
  </template>
  
  <script>
  export default {
    props: {
      result: [Number, String]
    }
  };
  </script>
  
  <style scoped>
  p {
    font-weight: bold;
    font-size: 22px;
    color: #4CAF50;
    margin-top: 30px;
  }
  </style>
  