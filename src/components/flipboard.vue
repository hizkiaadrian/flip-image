<template>
  <figure>
    <b-row>
      <b-btn variant="info" @click="flipVertical">Flip vertical</b-btn>
      <b-btn variant="info" @click="flipHorizontal">Flip horizontal</b-btn>
    </b-row>
    <img
      :src="url"
      alt="Image placeholder"
      v-bind:class="{
        flipVertically: verticalFlip,
        flipHorizontally: horizontalFlip
      }"
    />
  </figure>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "my-flipboard",
  props: {
    url: String
  },
  data() {
    return {
      verticalFlip: false,
      horizontalFlip: false
    };
  },
  methods: {
    flipVertical() {
      this.verticalFlip = !this.verticalFlip;
    },
    flipHorizontal() {
      this.horizontalFlip = !this.horizontalFlip;
    }
  }
});
</script>

<style scoped>
img {
  margin-bottom: 2rem;
  width: 50vw;
  border: 5px solid chocolate;
}

.row {
  justify-content: center;
}

.btn {
  margin: 0.5rem;
}

.flipVertically {
  -webkit-transform: scaleY(-1);
  -moz-transform: scaleY(-1);
  -o-transform: scaleY(-1);
  transform: scaleY(-1);
}

.flipHorizontally {
  -webkit-transform: scaleX(-1);
  -moz-transform: scaleX(-1);
  -o-transform: scaleX(-1);
  transform: scaleX(-1);
}
</style>
