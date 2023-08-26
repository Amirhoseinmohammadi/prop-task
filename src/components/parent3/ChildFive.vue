<template>
  <div class="m-2">
    <div class="border text-center py-2">
      <h2>Chlid 5</h2>
    </div>
    <div class="p-5 border">
      <p>name : {{ name }}</p>
      <button @click="changeName" class="btn btn-warning">
        change Child 1
      </button>
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

  methods: {
    changeName() {
      const changedName = "Ali"
      this.localName = changedName

      BusEvent.$emit("change", changedName)
    },
  },
}
</script>

<style lang="scss" scoped></style>
