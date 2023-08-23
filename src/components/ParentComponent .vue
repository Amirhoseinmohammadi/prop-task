<template>
  <div class="container border border-secondary my-5">
    <h1 class="">this parent component</h1>

    <div class="d-flex justify-content-between w-100">
      <div class="col-md-6 p-4 m-3 border border-secondary">
        <InputCompo :text="text" :number="number" @inputValues="setValues" />
      </div>
      <div class="col-md-6 p-4 m-3 border border-secondary w-50">
        <InputShow @dataPass="setInput" :text="text" :number="number" />
      </div>
    </div>
  </div>
</template>

<script>
import InputCompo from "./InputCompo.vue"
import InputShow from "./InputShow.vue"
export default {
  name: "ParentComponent",
  data() {
    return {
      text: "",
      number: "",
    }
  },

  components: {
    InputCompo,
    InputShow,
  },

  methods: {
    setValues(input) {
      this.text = input.text
      this.number = input.number
    },
    setInput(data) {
      this.text = data.text
      this.number = data.number
    },
  },
}
</script>
