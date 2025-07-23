<template>
  <NuxtLink
    :to="urlToRedirect"
    class="self-end bg-[#11B0C8] flex gap-2 py-[6px] pl-1 pr-2 rounded-[32px] text-sm items-center"
  >
    <IconsInfo />
    Saiba Mais
  </NuxtLink>
</template>

<script setup>
const props = defineProps({
  id: Number,
  type: {
    type: String,
    default: "character"
  }
});

const urlToRedirect = computed(() => {
  if (props.type === "character") {
    return `/character/${props.id}`;
  }

  return `/episode/${props.id}`;
});
</script>
