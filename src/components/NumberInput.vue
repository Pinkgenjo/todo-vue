<template>
    <input 
      type="number" 
      :placeholder="placeholder" 
      :value="modelValue" 
      @input="$emit('update:modelValue', $event.target.value)" 
    />
  </template>
  
  <script>
  export default {
    props: {
      modelValue: Number,
      placeholder: String
    }
  };
  </script>
  
  <style scoped>
  input {
    margin: 10px;
    padding: 12px;
    font-size: 18px;
    width: 250px;
    border: 2px solid #ccc;
    border-radius: 8px;
    transition: border 0.3s ease;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  input:focus {
    border-color: #4CAF50;
    outline: none;
  }
  
  input:hover {
    border-color: #4CAF50;
  }
  
  input::placeholder {
    color: #999;
    font-size: 16px;
  }
  </style>
  