<template>
  <b-container fluid class="main-content">
    <Flipboard v-if="url" :url="url" />
    <b-card
      v-else
      border-variant="dark"
      header-bg-variant="dark"
      header-text-variant="white"
      title="Flip Image"
      class="text-center w-50 p-5"
    >
      <b-card-text>
        Flip Image allows you to flip an image horizontally or vertically, or
        both. Start by either uploading a file or generating a random
        picture</b-card-text
      >
    </b-card>
    <input
      type="file"
      accept="image/jpeg, image/png"
      hidden
      ref="image-input"
      @change="changeFile"
    />
    <b-row>
      <b-btn variant="primary" @click="chooseFile">Upload an image</b-btn>
      <b-btn variant="primary" @click="generateRandomImage">
        Generate a random picture
      </b-btn>
    </b-row>
  </b-container>
</template>

<script>
import Vue from "vue";
import Flipboard from "./flipboard.vue";

export default Vue.extend({
  name: "my-main-content",
  components: { Flipboard },
  data: function() {
    return {
      imageCounter: 1,
      url: null
    };
  },
  methods: {
    chooseFile() {
      this.$refs["image-input"].click();
    },
    changeFile() {
      this.url = URL.createObjectURL(this.$refs["image-input"].files[0]);
    },
    generateRandomImage() {
      this.url = `https://picsum.photos/300/200?random=${this.imageCounter++}`;
    }
  }
});
</script>

<style scoped>
.main-content {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  justify-content: center;
  align-items: center;
  padding: 2rem 0;
}

.main-content .btn {
  margin: 0.5rem;
}

.card {
  margin: 2rem;
}
</style>
