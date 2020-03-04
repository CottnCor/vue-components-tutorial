<template>
  <base-layout class="home">
    <template v-slot:header>
      <reveal-word :content="title" />
    </template>
    <template v-slot:main>
      <common-form :title="title" />
    </template>
    <template v-slot:footer></template>
  </base-layout>
</template>

<script lang="ts">
import Vue from "vue";
import BaseLayout from "../layout/BaseLayout.vue";
import { RevealWord, CommonForm } from "../components";
export default Vue.extend({
  name: "home",
  components: {
    BaseLayout,
    RevealWord,
    CommonForm
  },
  data() {
    return {
      title: "sword art online"
    };
  }
});
</script>
