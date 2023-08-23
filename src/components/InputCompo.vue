<template>
  <div>
    <div class="container-fuild">
      <label for="input1">Name</label>
      <b-form-input
        id="input1"
        @input="emitValues"
        v-model="text"
        placeholder="Enter your name"
      ></b-form-input>

      <label for="input2">Number</label>
      <b-form-input
        id="input2"
        v-model="number"
        type="number"
        @input="emitValues"
        placeholder="Enter your id"
      ></b-form-input>
    </div>
  </div>
</template>

<script>
export default {
 
  data() {
    return {
      text: "",
      number: "",
    }
  },
  methods: {
    emitValues() {
      this.$emit("inputValues", { text: this.text, number: this.number })
    },
  },
}
</script>

<style lang="scss" scoped></style>
