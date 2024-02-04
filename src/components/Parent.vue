<script lang="ts" setup>
import Child from "./Child.vue";
</script>

<template>
  <div>Setup Component</div>
  <Child msg="Setup" v-slot="{ count, msg }">{{ count }} {{ msg }}</Child>
  <!-- count is number, msg is string -->
</template>
