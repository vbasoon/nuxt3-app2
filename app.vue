<template>
  <div class="wrapper">
    <TheHeader />
    <div class="main">
      <NuxtPage />
    </div>

    <TheFooter />
  </div>
</template>

<script setup></script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Roboto", sans-serif;
  font-size: 16px;
  color: #fff;
  background-color: #000;
}

h1 {
  text-align: center;
  font-size: 2rem;
  font-weight: bold;
  margin: 1rem 0;
}

.wrapper {
  max-width: 1440px;
  width: 100%;
  height: 100vh;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  background-color: #fff;
  color: #000;
}
.main {
  flex: 1;
}
</style>
