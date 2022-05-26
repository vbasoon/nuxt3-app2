<template>
  <div class="home px-4">
    <h1 class="text-center pt-3">Main Page</h1>
    <section class="section section-news border-blue">
      {{ news.articles }}
    </section>
    <section class="section section-news-hot border-blue">
      section news-hot
    </section>
    <section class="section section-news border-blue">section news</section>
    <section class="section section-hero border-blue">Hero section</section>
    <section class="section section-news-hot border-blue">
      section news-hot
    </section>
    <section class="section section-news border-blue">section stories</section>
    <section class="section section-news-big border-blue">
      section big images
    </section>
    <section class="section section-news-hot border-blue">
      section news-hot
    </section>
    <section class="section section-news-big border-blue">
      section big images
    </section>
    <section class="section section-news-bottom border-blue">
      section bottom
    </section>
  </div>
</template>

<script setup>
let news = [];

const url =
  "https://newsapi.org/v2/top-headlines?" +
  "country=ua&" +
  "apiKey=77ecb3d574ae41ddb93b7e13fdc4fba6";
news = await fetch(url).then((r) => r.json());
console.log(news.articles);
</script>

<style lang="scss">
.section {
  padding: 1rem;
  background: #062068;
  color: #fff;
  margin-bottom: 1rem;
}
</style>
