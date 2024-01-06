<template>
  <nav
    class="bg-green-200 px-20 py-20 container mx-auto px-3 h-24 flex items-center justify-between px-4 mb-20 space-y-10"
  >
    <NuxtLink to="/" class="h-44"
      ><NuxtImg
        src="/android-chrome-512x512.png"
        sizes="100vw sm:50vw md:200px"
      />
    </NuxtLink>
    <ul class="flex space-x-8 items-center">
      <NuxtLink to="/produits">
        <li>Produits</li>
      </NuxtLink>
      <NuxtLink to="/articles">
        <li>Articles</li>
      </NuxtLink>
      <NuxtLink
        to="/Contact"
        class="bg-orange-600 px-4 py-1 rounded-lg shadow hover:shadow-lg text-stone-50 text-xl"
      >
        <li>Contact</li>
      </NuxtLink>
      <NuxtLink to="/Equipe">
        <li>Equipe</li>
      </NuxtLink>
    </ul>
  </nav>
</template>
