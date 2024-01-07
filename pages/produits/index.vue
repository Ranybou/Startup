<script setup>
const query = gql`
  query Produits {
    produits {
      createdAt
      publishedAt
      titre
      slug
      updatedAt
      image {
        url(transformation: { document: { output: { format: webp } } })
      }
    }
  }
`;

const produits = ref();
const { data } = await useAsyncQuery(query);

console.log(data.value);
produits.value = data.value.produits;
</script>

<template>
  <li v-for="produit in produits" class="list-none">
    <NuxtLink :to="`/produits/${produit.slug}`">
      <h2 class="font-bold text-4xl text-center">
        {{ produit.titre }}
      </h2>
      <NuxtImg class="flex items-center justify-center" :src="produit.image.url" :alt="produit.titre" />
    </NuxtLink>
  </li>

</template>
