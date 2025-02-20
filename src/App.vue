<script setup>
import { ref, computed } from 'vue';

const num1 = ref(0);
const num2 = ref(0);
const operation = ref('+');

const result = computed(() => {
  switch (operation.value) {
    case '+': return num1.value + num2.value;
    case '-': return num1.value - num2.value;
    case '*': return num1.value * num2.value;
    case '/': return num2.value !== 0 ? num1.value / num2.value : 'Erro';
    default: return 0;
  }
});
</script>

<template>
  <div class="calculator">
    <h2>Calculadora Aritmética</h2>
    <input type="number" v-model.number="num1" placeholder="Número 1">
    <select v-model="operation">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">×</option>
      <option value="/">÷</option>
    </select>
    <input type="number" v-model.number="num2" placeholder="Número 2">
    <h3>Resultado: {{ result }}</h3>
  </div>
</template>

<style scoped>
body {
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f4f4f4;
  margin: 0;
}
.calculator {
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;
}
input, select {
  margin: 10px;
  padding: 5px;
  font-size: 18px;
}
</style>
