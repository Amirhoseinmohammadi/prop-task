<template>
  <div>
    <div class="text-center border my-2">
        <h1 class="my-2">This parent 3 component</h1>
      </div>
    <div class="d-flex flex-wrap justify-content-center mt-4">
      <ChildOne :name="name" />
      <ChildTwo :name="name" />
      <ChildThree :name="name" />
      <ChildFour :name="name" />
      <ChildFive :name="name" />
    </div>
  </div>
</template>

<script>
import ChildOne from "./ChildOne.vue"
import ChildTwo from "./ChildTwo.vue"
import ChildThree from "./ChildThree.vue"
import ChildFour from "./ChildFour.vue"
import ChildFive from "./ChildFive.vue"
export default {
  components: {
    ChildOne,
    ChildTwo,
    ChildThree,
    ChildFour,
    ChildFive,
  },

  data() {
    return {
      name: "Amirhosein",
    }
  },
}
</script>

<style lang="scss" scoped></style>
