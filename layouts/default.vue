<template>
  <div>
    <header class="title">
      <NuxtLink class="logo" to="/">Nuxt Shopping</NuxtLink>
    </header>
    <Nuxt />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
header {
  display: flex;
  padding: 0 0.5rem;
  height: 60px;
  align-items: center;
}
.logo {
  font-weight: 900;
}
.logo:visited {
  color: inherit;
}
</style>
