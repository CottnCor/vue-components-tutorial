<template>
  <div class="common-form-item">
    <span class="label" v-if="label">{{ label }}</span>
    <div class="input">
      <slot></slot>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "common-form-item",
  props: {
    label: {
      type: String,
      default: ""
    }
  }
});
</script>

<style lang="scss" scoped>
.common-form-item {
  display: flex;
  flex-direction: row;
  .label {
    width: max-content;
    padding-right: 0.5rem;
  }
  .input {
    padding-left: 0.5rem;
  }
}
</style>