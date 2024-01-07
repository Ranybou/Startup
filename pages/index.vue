<script setup>
const query = gql`
  query Accueil {
    page(where: { slug: "accueil" }) {
      slug
      titre
      texte {
        html
      }
    }
  }
`;


const accueil = ref();
const { data } = await useAsyncQuery(query);
console.log(data.value);
accueil.value = data.value.page;
</script>

<template>
  <h2  class="font-bold text-5xl text-center">
   
  </h2>

  <div class="font-bold text-4xl text-center" v-html="accueil.texte.html"></div>

</template>
