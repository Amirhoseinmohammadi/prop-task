<template>
  <div class="m-2">
    <div class="border text-center py-2">
      <h2>Chlid 1</h2>
    </div>
    <div class="p-5 border">
      <p>name : {{ localName }}</p>
      <button class="btn btn-danger">change</button>
    </div>
  </div>
</template>

<script>
import { BusEvent } from "@/main.js"
export default {
  props: {
    name: String,
  },

  data() {
    return {
      localName: this.name,
    }
  },
  created() {
    BusEvent.$on("change", (changedName) => {
      this.localName = changedName
    })
  },
}
</script>

<style lang="scss" scoped></style>
