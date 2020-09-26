<template>
  <b-card>
    <span class="footer-info">
      <span>Flip Image by Hizkia Adrian Susanto</span>
      <span class="social-icons">
        <a v-bind:href="'https://www.facebook.com/hizkiaadrians'">
          <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'facebook' }"
        /></a>
        <a v-bind:href="'https://github.com/hizkiaadrian'">
          <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'github' }"
        /></a>
        <a v-bind:href="'https://twitter.com/hizkiaadrian97'">
          <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'twitter' }"
        /></a>
        <a v-bind:href="'https://www.instagram.com/hizkia.susanto'">
          <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'instagram' }"
        /></a>
        <a
          v-bind:href="'https://www.linkedin.com/in/hizkia-susanto-3a849a162/'"
        >
          <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'linkedin' }"
        /></a>
      </span>
    </span>
  </b-card>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "my-footer"
});
</script>

<style scoped>
.card-body {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.footer-info {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.social-icons a {
  color: #000 !important;
}

.social-icons svg {
  margin: 0 8px;
}

.social-icons svg:hover {
  color: #e9e953;
  cursor: pointer;
}
</style>
