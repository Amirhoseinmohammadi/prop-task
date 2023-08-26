<template>
  <div class="m-2">
    <div class="border text-center py-2">
      <h2>Chlid 3</h2>
    </div>
    <div class="p-5 border">
      <p>name : {{ name }}</p>
      <button class="btn btn-danger">change</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    name: name,
  },
}
</script>

<style lang="scss" scoped></style>
