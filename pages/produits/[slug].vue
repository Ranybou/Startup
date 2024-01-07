<script setup>
const query = gql`
  query produit($slug: String!) {
    produit(where: { slug: $slug }) {
      titre
      texte {
        html
      }
    }
  }
`;

const produit = ref();

const route = useRoute();
const { data } = await useAsyncQuery(query, {
  slug: route.params.slug,
});

console.log(data.value);
produit.value = data.value.produit;
</script>

<template>
  <div v-if="produit" class="max-w-lg text-center">
    <h2 class="font-bold text-xl text-center">{{ produit.titre }}</h2>
  </div>
  <div v-else>
    <li>Loading...</li>
  </div>
</template>
