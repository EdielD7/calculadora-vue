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
  <div class="calculator container mt-3 bg-dark text-light shadow-md">
    <h2 class="mb-4">Calculadora Aritmética</h2>
    <input class="p-2" type="number" v-model.number="num1" placeholder="Número 1">
    <select class="p-2" v-model="operation">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">×</option>
      <option value="/">÷</option>
    </select>
    <input class="p-2" type="number" v-model.number="num2" placeholder="Número 2">
    <h3 class="mt-3">Resultado: {{ result }}</h3>
  </div>
</template>

<style scoped>
body {
  background-color: rgb(72, 156, 86);
}
.calculator {
  padding: 20px;
  text-align: center;
  border-radius: 8px;
}
input, select {
  margin: 10px;
  font-size: 18px;
  border: 1px solid #000;
  border-radius: 8px;
}
</style>
