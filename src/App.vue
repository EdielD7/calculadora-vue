<script setup>

</script>

<template>
  <div class="container">
    <header>
      <h1>Calculadora Aritmética</h1>
    </header>
    <div class="calculadora">
      <label for="operacao">Operação</label>
      <div class="operacao">
        <select class="">
          <option value="soma">Soma</option>
          <option value="subtracao">Subtração</option>
          <option value="multiplicacao">Multiplicação</option>
          <option value="divisao">Divisão</option>
        </select>
      </div>
      <input class="" type="number" placeholder="Digite o primeiro número" />
      <input class="" type="number" placeholder="Digite o segundo número" />
    </div>
    <div class="resultado">
      
    </div>
  </div>
</template>

<style scoped>
/* .container {
  margin: 0 auto;
  max-width: 800px;
  padding: 1rem;
} */
.calculadora {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
</style>
