<template>
  <b-navbar class="shadow" type="dark" variant="dark">
    <b-navbar-brand class="m-auto">{{ appTitle }}</b-navbar-brand>
  </b-navbar>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "my-navbar",
  props: {
    appTitle: String
  }
});
</script>

<style lang="scss" scoped></style>
