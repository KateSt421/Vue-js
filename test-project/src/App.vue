<template>
  <div id="app">
    <input v-model="operand1" />
    <input v-model="operand2" />
    <p>Результат: {{result}}</p>
    <div class="keyboard">
      <button v-on:click="result = +operand1 + +operand2">+</button>
      <button v-on:click="result = operand1 - operand2">-</button>
      <button @click="result = operand1 / operand2">/</button>
      <button @click="result = operand1 * operand2">*</button>
      <button @click="result = Math.pow(operand1, operand2)">Возведение в степень</button>
      <button @click="result = Math.round(operand1/operand2)">Целочисленное деление</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Calculator',
  data() {
    return {
      operand1: 0,
      operand2: 0,
      result: 0
    }
  }
}
</script>

<style lang="scss">

</style>
