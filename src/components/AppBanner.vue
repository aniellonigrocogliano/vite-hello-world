<script>
export default {
  data() {
    return {
      title: "Foto Random",
      image: "https://picsum.photos/300/200",
    };
  },
  methods: {
    getImagePath(imageName) {
      return new URL(`${imageName}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div class="banner">
    <h2>{{ title }}</h2>
    <img :src="getImagePath(image)" alt="Foto Random" />
  </div>
</template>

<style>

</style>