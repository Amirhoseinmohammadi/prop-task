<template>
  <div>
    <h3>ChildTwo</h3>
    <div class="w-85">
      <b-form @submit.prevent="onSubmit" @reset="onReset" v-if="show">
        <b-form-group
          id="input-group-1"
          label="Email address:"
          label-for="input-1"
          description="We'll never share your email with anyone else."
        >
          <b-form-input
            id="input-1"
            v-model="form.email"
            type="email"
            placeholder="Enter email"
            required
          ></b-form-input>
        </b-form-group>

        <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
          <b-form-input
            id="input-2"
            v-model="form.name"
            placeholder="Enter name"
            required
          ></b-form-input>
        </b-form-group>

        <b-button type="submit" variant="primary">Submit</b-button>
        <b-button type="reset" variant="danger">Reset</b-button>
      </b-form>
      <b-card class="mt-3" header="Form Data Result">
        <pre class="m-0">{{ form }}</pre>
        <pre >{{ newdata }}</pre>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    newdata: {
      type: Object,
    },
  },

  data() {
    return {
      form: {
        email: "",
        name: "",
      },

      show: true,
    }
  },
  methods: {
    onSubmit() {
      this.$emit("form-submitted", this.form)
    },
    onReset(event) {
      event.preventDefault()
      // Reset our form values
      this.form.email = ""
      this.form.name = ""
      this.form.food = null
      this.form.checked = []
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    },
  },
}
</script>

<style lang="scss" scoped></style>
