<template>
  <form>
    <p v-if="title">{{ title }}</p>
    <div class="common-form">
      <slot></slot>
    </div>
  </form>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "common-form",
  components: {},
  props: {
    title: {
      type: String,
      default: ""
    }
  },
  data() {
    return {
      fields: []
    };
  },
  mounted() {
    document.addEventListener("copy", function(e) {});
  },
  beforeDestroy() {},
  methods: {},
  computed: {},
  watch: {}
});
</script>

<style lang="scss" scoped>
.ccommon-form {
  display: flex;
  flex-direction: column;
}
</style>
