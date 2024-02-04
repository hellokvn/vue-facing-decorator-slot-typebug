<script lang="ts">
import { Component, Vue, Prop, toNative } from "vue-facing-decorator";

@Component
export default class Child extends Vue {
  @Prop()
  public readonly msg!: string;

  public count: number = 0;
}
</script>

<template>
  <div>Prop: {{ msg }}</div>
  <div>State: {{ count }}</div>
  <div>Slot: <slot :count="count" :msg="msg"></slot></div>
</template>
