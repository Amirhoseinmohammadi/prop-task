<template>
  <div id="app">
    <ParentComponent />
    <ParentTwo />
    <ParentThree/>
  </div>
</template>

<script>
import ParentComponent from "./components/ParentComponent .vue"
import ParentTwo from "@/components/nested/ParentTwo.vue"
import ParentThree from "@/components/parent3/ParentThree.vue"
export default {
  name: "App",
  components: {
    ParentComponent,
    ParentTwo,
    ParentThree,
  },
}
</script>

<style></style>
