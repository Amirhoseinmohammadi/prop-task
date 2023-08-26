<template>
  <div>
    <h2>ChildOne</h2>
    

    <div class="p-2">
      <b-table striped hover :items="items"></b-table>
    </div>
    <button class="btn btn-success" @click="passData">passToChild2</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [this.data],
    }
  },
  props: {
    data: {
      type: Object,
    },
  },
  methods: {
    passData() {
      this.$emit("passData", this.items)
    },
  
  },
}
</script>

<style lang="scss" scoped></style>
