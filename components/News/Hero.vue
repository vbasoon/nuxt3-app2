<template>
  <div>
    <div class="">
      <h1>News</h1>
    </div>
    <section>
      <img class="hero-image" :src="urlToImage" alt="" />
    </section>
  </div>

  <!-- <section class="section section-hero relative">
    <img class="hero-image" :src="news.articles[0].urlToImage" alt="" />
    <div class="hero-content">
      <h1 class="hero-title text-4xl">
        <slot name="title">{{ news.articles[0].title }}</slot>
      </h1>
      <p class="hero-text">
        <slot name="text">Text</slot>
      </p>
    </div>
  </section> -->
</template>

<script setup>
const props = defineProps({
  urlToImage: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss" scoped></style>
