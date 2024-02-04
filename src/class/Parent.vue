<script lang="ts">
import { Component, Vue } from "vue-facing-decorator";
import Child from "./Child.vue";

@Component({
  components: { Child },
})
export default class Parent extends Vue {}
</script>

<template>
  <div>Class Component</div>
  <Child msg="Class" v-slot="{ count, msg }">{{ count }} {{ msg }}</Child>
  <!-- count is any, msg is any -->
</template>
