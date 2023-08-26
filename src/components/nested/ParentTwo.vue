<template>
  <div>
    <div class="text-center border my-2">
      <h1 class="my-2">This parent 2 component</h1>
    </div>

    <div class="d-flex flex-wrap border p-3 justify-content-between">
      <div class="col-md-6 p-2 border">
        <ChildOne v-if="formdata" @passData="SetDataToClid2" :data="formdata" />
      </div>
      <div class="col-md-6 p-2 border">
        <ChildTwo :newdata="childData" @form-submitted="formOnSubmited" />
      </div>
    </div>
  </div>
</template>

<script>
import ChildOne from "/src/components/nested/ChildOne.vue"
import ChildTwo from "/src/components/nested/ChildTwo.vue"
export default {
  data() {
    return {
      formdata: null,
      childData: null,
    }
  },
  components: {
    ChildOne,
    ChildTwo,
  },
  methods: {
    formOnSubmited(data) {
      this.formdata = data
      
    },
    SetDataToClid2(passData) {
      this.childData = passData
    },
  },
}
</script>

<style lang="scss" scoped></style>
