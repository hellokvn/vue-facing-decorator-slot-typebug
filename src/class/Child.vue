<script lang="ts" generic="T">
import { Component, Vue, Prop, toNative } from "vue-facing-decorator";

@Component
export default class Child<T> extends Vue {
  @Prop()
  public readonly msg!: T;

  public count: number = 0;
}
</script>

<template>
  <div>Prop: {{ msg }}</div>
  <div>Ref: {{ count }}</div>
  <div>Slot: <slot :count="count"></slot></div>
</template>
