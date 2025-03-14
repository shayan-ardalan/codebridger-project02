
<template>
  <div>
    <nav class="nav">
   <NuxtLink to="/">خانه</NuxtLink>
     <NuxtLink to="/courses">دوره‌ها</NuxtLink>
    <NuxtLink to="/prices">قیمت‌ها</NuxtLink>
    </nav>
    <main class="main">
      <slot />
    </main>
  </div>
</template>

<style scoped>
.nav {
  padding: 1rem;
  background: #f1f1f1;
}
.nav a {
  margin: 0 1rem;
}
.main {
  padding: 2rem;
}
</style> 