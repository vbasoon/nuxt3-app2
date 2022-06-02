<template>
  <div>
    <div class="">
      <h1>Blogs</h1>
      <div class="container flex">
        <NewsGrid :articles="articles" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
