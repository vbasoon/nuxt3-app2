<template>
  <header class="flex justify-between">
    <NuxtLink class="logo" to="/">Logo</NuxtLink>
    <nav class="navbar">
      <NuxtLink to="/">Новости</NuxtLink>
      <NuxtLink to="/specials">Война</NuxtLink>
      <NuxtLink to="/articles">История</NuxtLink>
      <NuxtLink to="/blogs">Разбор</NuxtLink>
    </nav>
    <div class="buttons">
      <button>Search</button>
      <button>Login</button>
    </div>
  </header>
</template>

<script setup></script>

<style lang="scss" scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background: #062068;
  border-bottom: 1px solid #eaeaea;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: #333;
}

.navbar {
  display: flex;
  align-items: center;
}

.navbar > * {
  margin-right: 1rem;
}

.buttons {
  display: flex;
  align-items: center;
}

.buttons > * {
  margin-right: 1rem;
}
</style>
