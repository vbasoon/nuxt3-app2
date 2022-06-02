<template>
  <div class="home px-4">
    <h1 class="text-center pt-3">Main Page</h1>
    <section class="section section_news border-blue">
      <div v-if="pending">
        <div class="">Loading...</div>
      </div>
      <div class="cards" v-else>
        <div class="card" v-for="article in news.articles" :key="article.title">
          <img class="card__image" :src="article.urlToImage" alt="card-image" />
          <div class="mt-4">{{ article.author }}</div>
          <div>{{ article.title }}</div>
          <div></div>
        </div>
      </div>
    </section>
    <section class="section section-news-hot border-blue">
      section news-hot
    </section>
    <section class="section section-news border-blue">section news</section>
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

    <NewsHero v-bind="articles" />

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
/* const url =
  "https://newsapi.org/v2/top-headlines?" +
  "country=ua&" +
  "apiKey=77ecb3d574ae41ddb93b7e13fdc4fba6"; */

const url =
  "https://newsapi.org/v2/top-headlines?" +
  "country=ua&" +
  "apiKey=77ecb3d574ae41ddb93b7e13fdc4fba6";

//const { data: news } = useFetch(url);
//const { data: news } = await useAsyncData("articles", () => $fetch(url));

/* const { pending, data: news } = useLazyAsyncData("articles", () => $fetch(url));

watch(news, (newNews) => {
  // Because count starts out null, you won't have access
  // to its contents immediately, but you can watch it.
}); */

const { pending, data: news } = useLazyFetch(url);

watch(news, (newNews) => {
  // Because count starts out null, you won't have access
  // to its contents immediately, but you can watch it.
});
console.log(news);
</script>

<style lang="scss">
.section {
  padding: 1rem;
  background: #062068;
  color: #fff;
  margin-bottom: 1rem;
}

.section-hero {
  padding: 1rem;
  width: 100%;
  min-height: 600px;
  background: #062068;
  color: #fff;
  height: auto;
}

.hero-image {
  display: block;
  margin: 0 auto;
}

.hero-content {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 30px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  z-index: 100;
  color: #fff;
  padding: 1rem;
}

.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: flex-start;
  margin-top: 1rem;
  gap: 1rem;
}

.card {
  width: 30%;
  min-height: 370px;
  background: #fff;
  color: #062068;
  margin-bottom: 1rem;
  padding: 1rem;
  border-radius: 5px;

  .card__image {
    width: 100%;
    height: auto;
    border-radius: 5px;
  }
}
</style>
