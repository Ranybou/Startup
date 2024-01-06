<script setup>
const query = gql`
  query Produits {
    produits {
      slug
      titre
      texte {
        html
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
      <h2 class="text-xl text-center">
        {{ produit.titre }}
      </h2>
      <NuxtImg :src="article.image.url" :alt="article.titre" />
    </NuxtLink>
  </li>
</template>
