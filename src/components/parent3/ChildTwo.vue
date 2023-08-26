<template>
  <div class="m-2">
    <div class="border text-center py-2">
      <h2>Chlid 2</h2>
    </div>
    <div class="p-5 border">
      <p>name : {{ name }}</p>
      <button @click="changeName4" class="btn btn-info">change Chlid 4</button>
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
    changeName4() {
      const newName = "Mohammad"
      this.localName = newName
      BusEvent.$emit("changeNameFour", newName)
    },
  },
}
</script>

<style lang="scss" scoped></style>
