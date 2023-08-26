<template>
  <div class="container w-100">
    <div class="d-flex flex-column">
      <p class="text-primary">{{ text }}</p>
      <p class="text-danger">{{ number }}</p>
 
    </div>
  </div>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: "",
    },
    number: {
      type: String,
      default: "",
    },
  },
  methods: {
   
  },
}
</script>

<style lang="scss" scoped></style>
