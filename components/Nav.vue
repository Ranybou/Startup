
<template>
  
<nav
    class="bg-green-200 px-20 py-20 rounded-lg shadow hover:shadow-l container mx-auto px-40 h-24 flex items-center justify-between px-4 mb-20 space-y-5 text-stone-40 text-xl"
  >
    <NuxtLink to="/" class="h-44"
      ><NuxtImg
        src="/android-chrome-192x192.png"
        sizes="100vw sm:100vw md:200px"
      />
    </NuxtLink>
    <ul class="flex space-x-8 items-center">
      <NuxtLink to="/produits">
        <li class="hover:underline hover:text-white">Produits</li>
      </NuxtLink>
      <NuxtLink to="/articles">
        <li class="hover:underline hover:text-white">Articles</li>
      </NuxtLink>
      <NuxtLink
        to="/Contact"
        class="bg-orange-600 hover:bg-orange-700 px-4 py-1 rounded-lg shadow hover:shadow-lg text-stone-50 text-xl"
      >
        <li class="hover:text-black">Contact</li>
      </NuxtLink>
      <NuxtLink to="/Equipe">
        <li class="hover:underline hover:text-white">Equipe</li>
      </NuxtLink>
    </ul>
  </nav>
</template>
