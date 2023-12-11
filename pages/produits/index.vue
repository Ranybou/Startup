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
   
    <li v-for="produit in produits">
      <NuxtLink :to="`/produits/${produit.slug}`">
        <h2>
    {{ produit.titre }}
</h2>


<div v-html="produit.texte.html"></div>
</NuxtLink>
</li>

</template>