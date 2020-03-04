<template>
  <div class="container">
    <header class="shadow_power">
      <slot name="header"></slot>
    </header>
    <main>
      <slot name="main"></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "base-layout",
  data() {
    return {
      menu: {}
    };
  }
});
</script>

<style lang="scss" scoped>
.container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  background-image: map-get($default, linear_pure);
  header {
    height: 64px;
    display: flex;
    background-image: map-get($default, linear_primary_2);
  }
  main {
    flex: 1;
  }
  footer {
    height: 240px;
    background-image: map-get($default, linear_dark);
  }
}
</style>