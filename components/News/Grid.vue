<template>
  <div class="grid pa-8">
    <Card
      v-for="article in articles"
      :key="article.title"
      :title="article.title"
      :author="article.author"
    />
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  grid-gap: 1rem;
}
</style>
