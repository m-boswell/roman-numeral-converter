<template>
  <div id="app">
    <h1>Roman Numeral Converter</h1>
    <p>Please input a number to convert into a roman numeral</p>
    <RomanNumeralConverter />
  </div>
</template>

<script>
import RomanNumeralConverter from "@/components/RomanNumeralConverter";

export default {
  name: 'App',
  components: {
    RomanNumeralConverter
  }
}
</script>

<style>
#app {
  padding: 20%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
