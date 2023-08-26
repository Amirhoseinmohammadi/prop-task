<template>
  <div>
    <div class="container border border-secondary my-5 w-75">
      <div class="text-center border my-2">
        <h1 class="my-2">This parent 1 component</h1>
      </div>

      <div class="d-flex flex-wrap justify-content-between my-5 mx-2 w-100">
        <div class="col-md-6 border border-secondary">
          <InputCompo @inputValues="setValues" />
        </div>
        <div class="col-md-6 w-50 border border-secondary">
          <InputShow :text="text" :number="number" />
        </div>
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
  },
}
</script>
