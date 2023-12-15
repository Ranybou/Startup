<template>
  <div class="min-h-screen bg-green-400">
    <nav class="container mx-auto px-3 h-24 flex items-center mb-10">
      <NuxtLink to="/">
        <h1 class="text-5xl">Recyclope</h1>
      </NuxtLink>
      <ul>
      <NuxtLink to="/produits">
      <li> Produits </li>
    </NuxtLink>
    <NuxtLink to="/articles">
      <li> Articles </li>
    </NuxtLink>
    </ul>
    </nav>
   
    <div class="container mx-auto px-3">
      <slot></slot>
    </div>
  </div>
</template>
