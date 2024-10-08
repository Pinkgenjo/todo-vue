<template>
  <div id="app">
    <h1>Calculadora Aritmética</h1>
    
    <NumberInput v-model="numero1" placeholder="Número 1" />
    <NumberInput v-model="numero2" placeholder="Número 2" />
    
    <OperationSelect v-model="operacao" />
    
    <ResultDisplay :result="resultado" />
  </div>
</template>

<script>
import NumberInput from './components/NumberInput.vue';
import OperationSelect from './components/OperationSelect.vue';
import ResultDisplay from './components/ResultDisplay.vue';

export default {
  components: {
    NumberInput,
    OperationSelect,
    ResultDisplay
  },
  data() {
    return {
      numero1: '',
      numero2: '',
      operacao: 'soma'
    };
  },
  computed: {
  resultado() {
    const num1 = Number(this.numero1);
    const num2 = Number(this.numero2);

    switch (this.operacao) {
      case 'soma':
        return num1 + num2;
      case 'subtracao':
        return num1 - num2;
      case 'multiplicacao':
        return num1 * num2;
      case 'divisao':
        return num2 !== 0 ? num1 / num2 : 'Erro: Divisão por zero';
      default:
        return 0;
    }
  }
}
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f4f4f9;
}

h1 {
  color: #333;
  margin-bottom: 20px;
  font-size: 32px;
}

#app div {
  background-color: #fff;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}
</style>
