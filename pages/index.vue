<template>
  <div class="flex flex-col gap-16">
    <HomeHeroHeader />

    <PageContainer>
      <CharactersListing />

      <EpisodesListing />
    </PageContainer>
  </div>
</template>

<script lang="ts" setup>
import CharactersListing from "@/components/CharactersListing/index.vue";
import EpisodesListing from "@/components/EpisodesListing/index.vue";

useHead({
  title: `Rick And Morty API`
});
</script>
