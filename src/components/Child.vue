<script setup lang="ts">
defineProps<{ msg: string }>();

const count: number = 0;
</script>

<template>
  <div>Prop: {{ msg }}</div>
  <div>State: {{ count }}</div>
  <div>Slot: <slot :count="count" :msg="msg"></slot></div>
</template>
