<template>
  <h1> {{ message }} </h1>
  <hr />
  <h1>number: {{ number }}</h1>
  <hr>
  <h1>doubleNum(50): {{ doubleNum(50) }}</h1>
  <hr>
  <h1>nummber * 2: {{ number * 2 }}</h1>
  <hr>
  <h1>{{ number > 150? 'number is greater than 150': 'number is less than 150' }}</h1>
  <hr>
  <h1 v-text="number"></h1>
  <hr>
  <h1>{{ rawHtml }}</h1>
  <hr>
  <h1 v-text="rawHtml"></h1>
  <hr>
  <h1 v-html="rawHtml"></h1>
</template>

<script setup>
let message = 'Hello, Vue!'
let number = 50;

function doubleNum(num) {
  return num * 2;
}

let rawHtml = '<span style="color: red">This should be red.</span>'
</script>

<style lang="scss" scoped>

</style>