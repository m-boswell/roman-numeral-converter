<template>
  <div class="RomanNumeralConverter">
    <form class="RomanNumeralConverter__form">
      <div class="RomanNumeralConverter__field">
        <label for="number">Number:</label>
        <input type="number" id="number" name="number" v-model="number"/>
      </div>
    </form>
    <div v-if="romanNumeral">
      <h3>Output: <span>{{romanNumeral}}</span></h3>
    </div>
  </div>

</template>

<script>
import nomar from 'nomar';
export default {
  name: "RomanNumeralConverter",
  data() {
    return {
      number: ''
    }
  },
  computed: {
    romanNumeral() {
      if (this.number) {
        return nomar(Number.parseInt(this.number));
      }
      return false;
    }
  }
}
</script>

<style>
.RomanNumeralConverter__field {
  display: inline-flex;
  flex-direction: column;
}
.RomanNumeralConverter__field label {
  font-weight: bold;
  margin-bottom: 10px;
}

@media screen and (min-width: 750px) {
  .RomanNumeralConverter__field {
    flex-direction: row;
  }
  .RomanNumeralConverter__field label {
    margin-bottom: 0;
    margin-right: 20px
  }
}
</style>
