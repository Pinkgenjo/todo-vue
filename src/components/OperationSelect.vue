<template>
    <select :value="modelValue" @change="$emit('update:modelValue', $event.target.value)">
      <option value="soma">Soma</option>
      <option value="subtracao">Subtração</option>
      <option value="multiplicacao">Multiplicação</option>
      <option value="divisao">Divisão</option>
    </select>
  </template>
  
  <script>
  export default {
    props: {
      modelValue: String
    }
  };
  </script>

  <style scoped>
  select {
    margin: 10px;
    padding: 12px;
    font-size: 18px;
    width: 250px;
    border: 2px solid #ccc;
    border-radius: 8px;
    transition: border 0.3s ease;
    background-color: #fff;
    cursor: pointer;
  }
  
  select:focus {
    border-color: #4CAF50;
    outline: none;
  }
  
  select:hover {
    border-color: #4CAF50;
  }
  </style>
  