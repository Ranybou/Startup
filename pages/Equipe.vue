<script setup>
const query = gql`
  query Equipe {
    page(where: { slug: "equipe" }) {
      slug
      titre
      texte {
        html
      }
    }
  }
`;

const equipe = ref();
const { data } = await useAsyncQuery(query);
console.log(data.value);
equipe.value = data.value.page;
</script>

<template>
  <h2>
    {{ equipe.titre }}
  </h2>

  <div v-html="equipe.texte.html"></div>
</template>
