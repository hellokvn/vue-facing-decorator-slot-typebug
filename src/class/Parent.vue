<script lang="ts">
import { Component, Vue } from "vue-facing-decorator";
import Child from "./Child.vue";

@Component({
  components: { Child },
})
export default class Parent extends Vue {}
</script>

<template>
  <Child :msg="2" v-slot="{ count }">{{ count }}</Child>
</template>
